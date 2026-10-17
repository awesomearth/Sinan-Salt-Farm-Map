# Sources

All URLs were retrieved and read on 2026-10-13. Every figure in `salt_data.json` was checked against the downloaded page or PDF text, not against a search-engine summary. "Primary" means a government, public-research-institute or encyclopedic publication; "secondary" means a newspaper article. Secondary figures are flagged `"secondary": true` in the data and labelled as secondary in the page.

**Administrative note.** Since 2026 the official pages for Jeollanam-do appear under the name 전남광주통합특별시 (Jeonnam–Gwangju integrated special city). The sources describe the former Jeollanam-do area, so the data and the page keep the name "Jeollanam-do". Jeollabuk-do became Jeonbuk State (전북특별자치도) in January 2024.

**Definitions used in the data.** `basis: "total"` means licensed salt-pan area or licensed businesses, idle ones included (허가 면적 / 업체 수). `basis: "operating"` means producing area or producing businesses (가동·생산 면적 / 생산업체 수). `basis: "unspecified"` means the source does not say which. A "farm" (`farm_count`) is a salt-farm business (업체/개소), as the sources count them.

---

### S01 — 전국염전현황 (National salt-farm status)
- Publisher: Sinan-gun (신안군청), 천일염정보 section
- Year: 2025 data (page lists 2025 monthly figures; the Sinan 2025 output in the summary table matches the 2025 column)
- URL: https://www.shinan.go.kr/home/www/dept_info/economy/salt_info/salt_info_02/page.wscms
- Type: primary (county government)
- Supports: 2025 `farm_count` (total), `area_ha` (total), `production_t` for South Korea, Jeollanam-do and Sinan-gun; Sinan-gun `production_t` 2021–2025.
- Note: the Jeollanam-do area is printed "2.316"; it is read as 2,316 ha.

### S02 — 읍면별염전현황 (Salt farms by eup/myeon, Sinan-gun)
- Publisher: Sinan-gun (신안군청)
- Year: 2025 (current table on the site; totals 693 businesses, matching S01 for 2025)
- URL: https://www.shinan.go.kr/home/www/dept_info/economy/salt_info/page.wscms
- Type: primary (county government)
- Supports: Sinan-gun 2025 `farm_count` and `area_ha`, total and operating; the same for 13 eup/myeon (township level).
- Note: the table totals 1,871 ha; S01 gives 1,869 ha for Sinan.

### S03 — 전남(광주통합특별시) 천일염 MAP (Solar salt map, by si/gun)
- Publisher: Jeollanam-do provincial government, solar salt portal (now under 전남광주통합특별시청 수산유통가공과)
- Year: end of 2023 ("'23년말 기준"); page updated 2024-07-23
- URL: https://solarsalt.jeonnam.go.kr/main/cm/cntnts/cntntsView.do?mi=9090&cntntsId=55
- Type: primary (provincial government)
- Supports: 2023 operating `area_ha`, operating `farm_count` and `production_t` for Mokpo, Suncheon, Boseong, Haenam, Muan, Yeonggwang, Wando, Jindo and Sinan.

### S04 — 천일염산업의 현황과 정책과제 (The solar salt industry: status and policy tasks), KREI Research Paper D289
- Authors / publisher: Han Jae-hwan and Choi Byung-ok, Korea Rural Economic Institute (KREI)
- Year: June 2010
- URL: https://www.krei.re.kr/attach/pdf/605ba745-aca8-2a94-e054-b09928988b3c.PDF (mirror: https://repository.krei.re.kr/bitstream/2018.oak/19451/1/)
- Type: primary (public research institute); tables 3-2 and 3-3 cite the Korea Salt Producers' Association (대한염업조합)
- Supports: 2008 licensed and operating `area_ha` and `farm_count`, and 2007 and 2008 `production_t`, for South Korea, Jeollanam-do and eight Jeonnam si/gun (Sinan, Mokpo, Muan, Jindo, Wando, Haenam, Yeonggwang, Boseong). Also the 1963 Salt Management Act and the March 2008 reclassification of solar salt as food.
- Note: Boseong's licensed business count is blank in table 3-3. The value 8 comes from S05.

### S05 — 미세여과방식 천일염 생산 공정 체계 기반 기능성 소금 대량생산 기획 연구 (Planning study, report PE9969E-000-00)
- Publisher: Korea Institute of Ocean Science and Technology (KIOST)
- Year: December 2018
- URL: https://sciwatch.kiost.ac.kr/bitstream/2020.kiost/36765/1/ (PDF "미세여과방식_천일염_생산_공정_체계_기반_기능성_소금_대량생산_기획_연구.pdf")
- Type: primary (public research institute). Tables 1-3, 1-5 and 1-6 cite Mokpo National University, 한국 천일염 기초과학연구소 조성사업 (2011). Table 1-10 cites the Ministry for Food, Agriculture, Forestry and Fisheries.
- Supports: Jeollanam-do and national `production_t` for every year 1990–2010; Boseong 2008 licensed `farm_count` (8); import liberalisation on 1 July 1997; the 2003 low of 155,951 t.
- Note: the 1990–1996 national figures are headed 소금생산량 (salt production). They may include salt other than solar salt.

### S06 — 지속가능한 전남 천일염산업을 위한 육성 과제 (Tasks for a sustainable Jeonnam solar salt industry), JNI Issue Report No. 63
- Author / publisher: Park Eun-ok, Jeonnam Research Institute (전남연구원)
- Year: 18 March 2026
- URL: https://mnuk2.mokpo.ac.kr/bbs/iacftmp/1182/256121/download.do (copy of the report hosted on a Mokpo National University board)
- Type: primary (provincial research institute). Table 3 cites Sinan-gun internal data (2026).
- Supports: Jeollanam-do `production_t` for 2011, 2013, 2020, 2021 and 2022 (given in thousand tonnes); 2025 operating `farm_count` and `area_ha` for Jeollanam-do and South Korea. Corroborates the 1990, 1994, 2008 and 2010 Jeonnam output in S05. Causes: import liberalisation (1997) and closure support (1997–2004); more rain days, conversion to solar power and an ageing workforce in the 2020s.
- Notes: table 3 prints 2,146 ha for both total and operating Jeonnam area. Only the operating figure is used, and S01's 2,316 ha total is kept. The report calls 1994 (378 kt) the peak, then gives 382 kt for 2013. Both figures are recorded as printed.

### S07 — 염전 (Salt farm), Encyclopedia of Korean Culture (한국민족문화대백과사전)
- Author / publisher: Han Ju-seong (2011, last revised 21 Aug 2026), Academy of Korean Studies
- URL: https://encykorea.aks.ac.kr/Article/E0037139
- Type: primary (scholarly encyclopedia; cites provincial statistical yearbooks and the Korea Salt Producers' Association)
- Supports: national context only. 1955: 10,500 ha and 350,000 t. 1985: 12,000 ha, 35.4% of it in Jeollanam-do, recorded as a note because no hectare figure is given. Repeal of the salt monopoly (30 Dec 1961, privatised 1 Jan 1962).
- Not used: the 1965 figure (2,000 ha) conflicts with the 1955 figure in the same article. The 2005 (11,190 ha) and 2009 (10,502.8 ha) figures are far above S04's 2008 licensed area (4,649 ha) and appear to be cadastral land-category (지목) area.

### S08 — 우리나라 소금의 역사 (History of salt in Korea)
- Publisher: Jeollanam-do solar salt portal
- Year: page updated 2022-11-17
- URL: https://solarsalt.jeonnam.go.kr/main/cm/cntnts/cntntsView.do?mi=9102&cntntsId=65
- Type: primary (provincial government)
- Supports events only: 1955 self-sufficiency (350,000 t); new salt-farm permits in 1964–65 and 1972; import liberalisation and closure subsidies 1997–2005; 2008 reclassification as food.

### S09 — 전남 염전·천일염 생산량 급속히 감소 (Jeonnam salt farms and output decline rapidly)
- Publisher: Naeil Shinmun (내일신문), reporter Bang Guk-jin
- Year: 3 August 2021
- URL: https://m.naeil.com/news/read/394607
- Type: **secondary** (newspaper, citing Jeollanam-do provincial salt-farm status data)
- Supports: Jeollanam-do 2016 and 2020 `area_ha` and `farm_count` (basis not stated); 2016 `production_t` (293,215 t); 2020 output 164,539 t, which corroborates S06's 165 kt. Causes: a 54-day monsoon in 2020, conversion to solar farms, an ageing workforce.

### S10 — 전북지역 염전이 사라지고 있다 (Salt farms are disappearing in Jeonbuk)
- Publisher: Jeonbuk Domin Ilbo (전북도민일보), reporter Kim Jong-ha
- Year: 18 July 2001
- URL: http://www.domin.co.kr/news/articleView.html?idxno=609358
- Type: **secondary** (newspaper, citing the Jeollabuk-do provincial government)
- Supports: Jeonbuk province 1999 and 2001 `farm_count`, `area_ha` and `production_t`; Gunsan 2001 `farm_count` (the article names all three remaining farms as being in Gunsan). Causes: cheap Chinese salt and conversion of salt-farm land, including an F1 Grand Prix site.
- Conflict: S12 says the Haeri salt farm in Gochang still held about 2.14 km² of salt pans in 2002. The article says only traces remained in Gochang and Buan. Both are recorded as written.

### S11 — 곰소 염전 (Gomso salt farm), Digital Buan Culture Encyclopedia (디지털부안문화대전)
- Author / publisher: Jo Seong-uk, Academy of Korean Studies
- URL: https://buan.grandculture.net/buan/toc/GC08000259
- Type: primary (scholarly local encyclopedia)
- Supports: site-level only. 1946: 892,562 m² and 9,000 t a year. In 1996, half (446,281 m²) was converted to other uses. These are single-farm figures, not Buan-gun totals.

### S12 — 해리염전 (Haeri salt farm), Encyclopedia of Korean Culture
- Publisher: Academy of Korean Studies
- URL: https://encykorea.aks.ac.kr/Article/E0062573
- Type: primary (scholarly encyclopedia)
- Supports: site-level only. 1948: 522,645 m². 1953: about 2.97 km². 2002: about 2.14 km² after a sale. Single farm, not Gochang-gun totals.

### S13 — 신안천일염 역사 (History of Sinan solar salt)
- Publisher: Sinan-gun (신안군청)
- Year: page dated 2016-09-26
- URL: https://www.shinan.go.kr/home/www/dept_info/economy/salt_info/salt_info_10/page.wscms
- Type: primary (county government; cites 신안비금 향토자료집, 1999)
- Supports events only: the first solar salt pan in Bigeum (1946), spreading from 1947; expansion through national land-development projects from the late 1970s and island development from the late 1980s.

### S14 — 천일염 현황 (Solar salt status by eup/myeon), KOSIS table DT_752001_E000001
- Publisher: Sinan-gun (전라남도 신안군), in its basic statistics on KOSIS (orgId 752)
- Year: 2018–2024 data; KOSIS shows the table as last updated 2026-06-02
- URL: https://kosis.kr/statHtml/statHtml.do?orgId=752&tblId=DT_752001_E000001 (figures were verified against a CP949-encoded KOSIS download of this table; the download is not included in this repository, but the table can be downloaded from the URL above)
- Type: primary (county government statistics on the national portal)
- Supports: for Sinan-gun and each of its 14 eup/myeon, 2018–2024: licensed and operating producers (생산자수, persons), licensed and operating salt-pan area, and output (tonnes).
- Notes: KOSIS's own legend defines "-" as 자료없음 (no data). Heuksan-myeon is "-" in every cell, and Anjwa-myeon's 2019 output is "-". These are recorded as gaps, not zeros. Aphae-eup's 2022 operating area (140.7 ha) is published as larger than its licensed area (115.3 ha) and is kept as published. For 2022, the Sinan total output is 203,244 t, while S01 gives 203,234 t. The 2024 values were checked against the live KOSIS table on 2026-10-13.

### S15 — 국내 천일염 생산현황 · 전국 염전 세부현황 (Salt farms by si/gun, licensed and operating)
- Publisher: Ministry of Oceans and Fisheries (해양수산부). The table credits Mokpo National University industry-academic cooperation (목포대 산학협력단, 소금산업 실태조사)
- Year: 2019, as given in the file name "천일염 제조업 현황(2019)". The PDF was created 19 Feb 2020 (author "mof").
- URL: https://www.mof.go.kr/jfile/readDownloadFile.do?fileType=MOF_ARTICLE&fileTypeSeq=30499&fileNum=1 (figures were verified against a downloaded copy; the PDF is not included in this repository, but it can be downloaded from the URL above)
- Type: primary (central government)
- Supports: licensed and operating salt-farm sites (염전 개소) and area (ha) for all 19 salt-producing si/gun in five provinces, the provincial subtotals and the national total. This adds Jeonbuk si/gun data: Gunsan 1 site / 3.8 ha, Buan 1 / 57.8 ha, Gochang 2 / 260.5 ha.
- Notes: Incheon Jung-gu's operating area (221.2 ha) is printed larger than its licensed area (34.4 ha) and is kept as printed. Sinan in 2019 is 840 sites / 2,612.2 ha licensed here, against 883 producers / 2,744 ha in S14. The counts use different units, and the areas are a genuine conflict between sources.

---

### Searched but not used
- **KOSIS (Statistics Korea), national tables.** Keyword searches for 염전, 천일염 and 소금생산 did not surface Sinan-gun's own table (S14), which was located separately. No national or provincial salt-farm table was found. KOSIS also has cadastral land-category tables (행정구역별·지목별 국토이용현황_시군구, 2007–2025) that include a "염전" land category. That category records land registered as salt farm, including abandoned pans, so it does not measure salt farms in operation and was not used.
- **Ministry of Oceans and Fisheries.** Apart from S15, no downloadable multi-year salt-production series was found.
- **News figures with a primary equivalent** (e.g. edaily 2020, Hankook Ilbo 2013, KMI global news 2016) were not used.
- **Sinan "2,671 ha" (Naeil 2021).** No year is attached, so it was not used.
- **Taepyeong salt farm 462 ha / 28,000 t (korea.kr).** The article is undated and the figures are single-site, so they were not used.
- No source URL was unreachable.

---

## Required external resources

| Resource | Purpose | Source/URL | License | Obtained? |
|---|---|---|---|---|
| Sinan-gun eup/myeon boundaries, plus neighbouring mainland si/gun as grey context | Map geometry | KOSTAT SGIS 2018 census boundaries via `southkorea/southkorea-maps` (https://github.com/southkorea/southkorea-maps): `kostat/2018/json/skorea-submunicipalities-2018-geo.json` filtered to codes 36480* (14 eup/myeon; islands under 0.04 km² dropped; simplified 12%), and `skorea-municipalities-2018-geo.json` for 10 nearby Jeonnam si/gun (simplified 5%). Simplified with mapshaper 0.6, combined into one quantised TopoJSON, embedded inline (~88 KB) | KOGL Type 1 (공공누리 제1유형): free use including modification and commercial use, attribution required (credit: 통계청 SGIS). Stated in the repository's `kostat/2018/json/LICENSE.md` | Y |
| Base map tiles | none used. The map is a self-contained vector map, so it needs no tile provider, network or tile attribution | n/a | n/a | Y (not needed) |
| D3.js 7.9.0 | Projection, paths, scales, chart | https://cdn.jsdelivr.net/npm/d3@7.9.0/dist/d3.min.js | ISC | Y (CDN at runtime) |
| topojson-client 3.1.0 | Decode embedded TopoJSON | https://cdn.jsdelivr.net/npm/topojson-client@3.1.0/dist/topojson-client.min.js | ISC | Y (CDN at runtime) |
| Fonts: IBM Plex Sans, IBM Plex Sans KR, IBM Plex Mono | Text, Hangul, figures | Google Fonts stylesheet https://fonts.googleapis.com/css2 (files from fonts.gstatic.com); falls back to system sans / Hangul / monospace fonts if offline | SIL Open Font License 1.1 | Y (CDN at runtime) |
| Images / photographs | none, by design | n/a | n/a | Y (none used) |
| Salt statistics | Embedded inline from `salt_data.json` | S01–S15 above | Government and encyclopedia pages: KOGL or publisher terms, cited; newspaper figures cited as facts only | Y |

Every external resource the page needs is listed above and is either loaded from a public CDN or embedded in `index.html`.
