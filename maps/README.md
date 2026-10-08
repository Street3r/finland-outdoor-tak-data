# Maps

National park maps: GeoPDF base maps and overlay KMZ files.

| What | Where | Naming |
|---|---|---|
| GeoPDF (large) | [Releases](../../../releases), tag `maps-YYYY.MM` | `<area>_<scale>_<YYYY-MM>.pdf`, e.g. `nuuksio_25k_2026-10.pdf` |
| Overlay KMZ | `maps/<category>/<area>/` | `<area>_overlay.kmz` |
| Sources and licence | `maps/<category>/<area>/SOURCES.md` | |
| Catalogue | [catalog.yaml](catalog.yaml) | one entry per map |

Release assets have stable URLs:
`https://github.com/Street3r/finland-outdoor-tak-data/releases/download/<tag>/<file>`

## Adding a map

1. Check that every source may be redistributed (e.g. National Land Survey of Finland data: CC BY 4.0). Do not publish material without a licence that allows it.
2. Create or update the release `maps-YYYY.MM` and upload the GeoPDF.
3. Put the overlay KMZ and `SOURCES.md` in `maps/<category>/<area>/`.
4. Add the map to `catalog.yaml`.

## Using GeoPDF in ATAK

Import Manager → select the `.pdf` → it appears under Overlay Manager → Imagery / Maps and works offline. Large files: copy to `atak/imagery/` on the device instead of importing.
