# Sinan's Salt Fields · 신안군 천일염전

An interactive, single-page data story about the solar salt farms (천일염전) of Sinan-gun, Jeollanam-do, South Korea. It maps the county's salt farms by eup/myeon (township) for every year with published figures, from 2018 to 2025. Built with Claude Code. 

Every number on the page traces to a cited source. Nothing is interpolated or estimated, and missing values are shown as missing, never as zero.

## Viewing the page

There is no build step. The page is one HTML file with the data and map geometry embedded.

- **Locally:** download or clone the repository and open `index.html` in a browser. An internet connection is needed for the JavaScript libraries and web fonts, which load from public CDNs.
- **GitHub Pages:** https://awesomearth.github.io/Sinan-Salt-Farm-Map/. 

## What the page shows

| Section | Content |
|---|---|
| 01 · Salt farms by eup/myeon | Choropleth map of Sinan's 14 eup/myeon, switchable between output, operating area, licensed area and operating producers. Years run 2018–2025, with playback. A linked panel ranks the eup/myeon and summarises any one you select. |
| 02 · Trends | Output, licensed versus operating salt-pan area, and licensed versus operating producers, for the selection or the whole county. |
| 03 · Composition | Output by eup/myeon, 2018–2024, as stacked bars. Clicking a block selects that eup/myeon across the page. |
| 04 · Context | All 19 salt-producing si/gun in Korea in 2019, and Jeollanam-do si/gun in 2008 against 2023. |
| 05 · Long run | Jeollanam-do and national output since 1990, with events that the sources document. |
| 06 · Method and sources | Definitions, the full table of figures used, and the numbered source list. |

The layout works at desktop, tablet and phone widths. Controls can be operated by keyboard, and the page respects reduced-motion settings.

## Data

`research/salt_data.json` holds **805 records** drawn from **15 sources**: government statistics, public research institutes, scholarly encyclopedias and, where nothing else covers a figure, two newspaper reports flagged as secondary. Full citations, URLs and notes are in [`research/SOURCES.md`](research/SOURCES.md).

The main sources are:

| ID | Source | Covers |
|---|---|---|
| S14 | Sinan-gun, *천일염 현황*, KOSIS table DT_752001_E000001 | Sinan and its 14 eup/myeon, 2018–2024: producers, licensed and operating area, output |
| S01, S02 | Sinan-gun county website | Sinan output 2021–2025; national, provincial and eup/myeon figures for 2025 |
| S15 | Ministry of Oceans and Fisheries, salt farms by si/gun (2019) | Licensed and operating sites and area for all 19 salt-producing si/gun |
| S03 | Jeollanam-do solar salt portal | Si/gun figures, end of 2023 |
| S04 | Korea Rural Economic Institute, Research Paper D289 (2010) | Si/gun figures for 2007–2008 |
| S05 | Korea Institute of Ocean Science and Technology (2018) | Jeollanam-do and national output, 1990–2010 |
| S06 | Jeonnam Research Institute, Issue Report No. 63 (2026) | Recent provincial output and documented causes of decline |

### Data rules

- **Nothing is invented.** No figure is interpolated, estimated, or shared out from a province total to its counties.
- **Missing is not zero.** Gaps are hatched on the map and marked "no data" elsewhere. In KOSIS tables, "-" means 자료없음 (no data) and is treated that way.
- **Licensed is not operating.** Licensed figures include idle salt pan and producers; operating figures do not. The two are never merged.
- **Count units are kept apart.** The KOSIS table counts producers (생산자수, persons); other sources count businesses or sites (업체 / 개소). The page does not compare across the two.
- **Calculated figures are labelled.** Changes since 2018, shares of the county total and ranks are calculated from two cited figures and marked "calculated".
- **Conflicts are kept, not resolved.** Where sources disagree, both values are recorded and the difference is noted.

### Known gaps

The full list is in [`research/GAPS.md`](research/GAPS.md). In short:

- No Jeolla province or county figures were found for any year before 1990.
- Heuksan-myeon has no salt-farm data in any year.
- No eup/myeon output has been published for 2025, though the county total exists.
- Jeonbuk State has province figures only for 1999 and 2001, from a newspaper report.

### Record format

Each record in `salt_data.json` looks like this:

```json
{
  "region_ko": "신의면",
  "region_en": "Sinui-myeon (Sinan)",
  "province": "Jeollanam-do",
  "year": 2024,
  "metric": "production_t",
  "value": 42750,
  "source_id": "S14",
  "level": "township",
  "basis": "operating",
  "geo_key": "3648038"
}
```

- `metric` is one of `production_t` (tonnes), `area_ha` (hectares) or `farm_count`.
- `level` is one of `national`, `province`, `county`, `township` or `site`.
- `basis` is `total` (licensed, idle included), `operating`, or `unspecified`.
- `geo_key` is the KOSTAT 2018 administrative code used to join records to the map.
- Optional fields: `count_unit` (`producers` or `businesses`), `note`, `corroborated_by` (other sources that report the same value) and `secondary` (true for newspaper sources).

## Repository structure

```
index.html              The page: HTML, CSS and JavaScript, with data and geometry embedded
research/
  salt_data.json        The compiled dataset (805 records, plus documented events)
  SOURCES.md            Full citations, notes per source, and external resources
  GAPS.md               Every region/year/measure combination without data, and source conflicts
```

The page embeds its own copy of the data. If you edit `research/salt_data.json`, update the `const DATA = …` line in `index.html` to match. That line holds the same `records` and `events` arrays.

## Built with

- [D3.js](https://d3js.org) 7.9.0 and [topojson-client](https://github.com/topojson/topojson-client) 3.1.0, loaded from jsDelivr
- Newsreader, IBM Plex Sans, IBM Plex Sans KR and Noto Serif KR, from Google Fonts
- No framework, bundler or server

## Attribution

- **Boundaries:** Statistics Korea (KOSTAT) SGIS census boundaries, 2018, via [southkorea/southkorea-maps](https://github.com/southkorea/southkorea-maps). Used under the Korea Open Government License Type 1 (공공누리 제1유형), which requires attribution. The boundaries were filtered to Sinan-gun and neighbouring si/gun, and simplified.
- **Statistics:** each figure is credited to its publisher on the page and in `research/SOURCES.md`.
- **Software and fonts:** D3.js and topojson-client are under the ISC License. The fonts are under the SIL Open Font License 1.1.

## A note on names

Since 2026, official Jeollanam-do websites appear under the name 전남광주통합특별시. This project uses "Jeollanam-do" for the area its sources describe. Jeollabuk-do became Jeonbuk State (전북특별자치도) in January 2024.

## License

- **Code** (the HTML, CSS and JavaScript in `index.html`) is released under the [MIT License](LICENSE).
- **The compiled dataset and original written content** (`research/salt_data.json`, `research/SOURCES.md`, `research/GAPS.md`, and the page text) are released under [Creative Commons Attribution 4.0 International](LICENSE-DATA).

**Third-party material is not covered by either license.** That includes the underlying statistics and source documents, the boundary data, the libraries and the fonts. It remains under its owners' terms, as listed above. Copies of source documents (PDF reports, KOSIS downloads) are not included in this repository; every source can be retrieved from the links in `research/SOURCES.md`.

## Disclaimer

This is an independent project, not affiliated with Sinan-gun, Statistics Korea, the Ministry of Oceans and Fisheries or any other source organisation. Figures are reproduced as their sources published them, as of 13 October 2026, including discrepancies between sources. Check the original sources before relying on any figure.

## Citation

> *Sinan's Salt Fields (신안군 천일염전): an interactive data story on Sinan-gun's solar salt farms, 2018–2025.* 2026. Data compiled from Statistics Korea (KOSIS), Sinan-gun, the Ministry of Oceans and Fisheries, and other sources listed in `research/SOURCES.md`.
