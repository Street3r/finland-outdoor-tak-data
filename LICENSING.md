# Licences

Different parts of this repository are licensed differently. The main licence of the repository, for the generated data, is the ODbL 1.0 in [LICENSE](LICENSE).

| Part | Licence |
|---|---|
| Generated data (`data` branch: KML, KMZ, data packages, GPX, index files) | [Open Database License (ODbL) 1.0](LICENSE) |
| Icon set (`iconset/`) | MIT, see [python-lipas2tak-tool](https://github.com/Street3r/python-lipas2tak-tool/blob/main/LICENSE) |
| Maps (`maps/`, GeoPDF releases) | per map, listed in [maps/catalog.yaml](maps/catalog.yaml) and the map's `SOURCES.md` |
| Documentation (`README.md`, `docs/`, `SHARE.md`) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| Tools (`tools/`, `.github/`) | [MIT](#mit-licence) |

## Generated data – ODbL 1.0

The generated data combines sources under different licences. Because it contains OpenStreetMap data, the combined database is made available under ODbL 1.0. CC BY 4.0 sources are included with their attribution preserved.

**Attribution** (keep this when you use or share the data):

> Lipas – University of Jyväskylä (CC BY 4.0); © OpenStreetMap contributors (ODbL 1.0); Statistics Finland (CC BY 4.0)

| Source | Used for | Licence |
|---|---|---|
| [Lipas](https://lipas.fi), University of Jyväskylä | sites, routes, national park boundaries | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |
| [OpenStreetMap](https://www.openstreetmap.org/copyright) | supplementary shelters, fire pits, towers, toilets | [ODbL 1.0](https://opendatacommons.org/licenses/odbl/1-0/) |
| [Statistics Finland](https://stat.fi) | region boundaries (grouping only) | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) |

Lipas citation: Lamberg, Anne; Laakso, Tapani. *Lipas data*. University of Jyväskylä. <https://doi.org/10.17011/jyx/dataset/110418>

In short: attribute the sources; if you publicly share a modified version of the data, share it under ODbL 1.0 as well. Maps and screenshots made with the data only need the attribution. The attribution is also embedded in every generated file.

## Maps

Each map lists its sources and licence in `maps/catalog.yaml` and in its `SOURCES.md`. Typical sources:

| Source | Licence | Attribution |
|---|---|---|
| National Land Survey of Finland (Maanmittauslaitos), topographic map / database | [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) | "Contains data from the National Land Survey of Finland Topographic Database MM/YYYY" |
| Data from this repository | ODbL 1.0 | as above |

Only material that may be redistributed is published here.

## MIT licence

Copyright (c) 2026 Street3r

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Disclaimer

The data and maps are provided as is, without warranty. Locations, services and route conditions may be outdated or wrong.
