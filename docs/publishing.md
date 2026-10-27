# Publishing

## Generated data (`data` branch)

- Written by the publisher in [docker-lipas-integration](https://github.com/Street3r/docker-lipas-integration) after each weekly run (enabled with `COMPOSE_PROFILES=github`).
- The publisher builds a separate public version with the project's own icon set and the GitHub Pages base URL.
- The branch is **replaced on every update** (single commit, force-push), so it only holds the latest version. `CHANGELOG.md` on the branch keeps a short history of changes.
- When no data changed, only the check time (`status.json`, index files) is updated; the changelog gets no new entry.
- Do not edit the `data` branch by hand.

Write access: a deploy key with write access. The publisher only pushes to the `data` branch, but a deploy key's write access covers the whole repository. The `protect-main` ruleset (Restrict deletions, Block force pushes) keeps `main` from being deleted or overwritten; the key could still add ordinary commits to `main`, so keep it only on the publishing server.

## Monitoring

The *Stale data check* workflow runs daily. If `status.json` on the `data` branch is more than 8 days old (a missed Monday run is reported on Tuesday), it opens an issue (GitHub e-mails the owner) with the commands to check on the server, and closes it when updates resume. It also opens an issue when the publisher blocked an update because the new build had far fewer features than the published data (`publish_blocked` in `status.json`); the published data stays as it was until a normal update or `--allow-shrink`. A third issue, *Data quality warnings*, lists the build's quality findings (`warnings` in `status.json`: areas without features, area names missing from `area_names.yaml`, very large files, source failures such as OSM data taken from the cache, areas missing since the previous build, and areas or kinds with far fewer features than before); it is updated daily and closed when the findings are gone. Dependabot keeps the workflow actions up to date. GitHub disables scheduled workflows of a public repository after 60 days without activity; the workflow re-enables itself through the API on every run to prevent that, but if the checks ever stop, see Actions → *Stale data check* → *Enable workflow*.

## GitHub Pages

Settings → Pages → Deploy from a branch → `data` / root. On a free GitHub plan Pages requires a public repository. Base URL: `https://street3r.github.io/finland-outdoor-tak-data/`.

The base URL is written into the KML network links and QR codes. Changing it later (e.g. to a custom domain) means users have to re-add their links, so decide before sharing widely.

## Maps (GeoPDF, overlays)

See [maps/README.md](../maps/README.md).

## QR codes

Per-area QR codes and share pages (`share/<lang>/`) are generated with the data. The start links on `main` are maintained here:

1. Add or edit an entry in [share/links.yaml](../share/links.yaml).
2. Run `python tools/make_qr.py` (needs `pip install segno pyyaml`), or let the workflow do it on push.
3. QR codes are written to `share/qr/` and listed in [SHARE.md](../SHARE.md) and [SHARE.fi.md](../SHARE.fi.md).
