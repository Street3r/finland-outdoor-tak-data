# Publishing

## Generated data (`data` branch)

- Written by the publisher in [docker-lipas-integration](https://github.com/Street3r/docker-lipas-integration) after each weekly run (`PUBLISH_GITHUB=true`).
- The publisher builds a separate public version with the project's own icon set and the GitHub Pages base URL.
- The branch is **replaced on every update** (single commit, force-push), so it only holds the latest version. `CHANGELOG.md` on the branch keeps a short history of changes.
- Nothing is pushed if no file changed.
- Do not edit the `data` branch by hand.

Write access: a deploy key with write access, used only for the `data` branch. Protect `main` with a ruleset so the key cannot change it.

## GitHub Pages

Settings → Pages → Deploy from a branch → `data` / root. Base URL: `https://street3r.github.io/finland-outdoor-tak-data/`.

The base URL is written into the KML network links and QR codes. Changing it later (e.g. to a custom domain) means users have to re-add their links, so decide before sharing widely.

## Maps (GeoPDF, overlays)

See [maps/README.md](../maps/README.md).

## QR codes

1. Add or edit an entry in [share/links.yaml](../share/links.yaml).
2. Run `python tools/make_qr.py` (needs `pip install segno pyyaml`), or let the workflow do it on push.
3. QR codes are written to `share/qr/` and listed in [SHARE.md](../SHARE.md).
