# Singapore Future MRT Station Triangulator & Property Alpha WebGIS (`v3`)

**Live Interactive WebGIS:** https://lauyeehow1986-hub.github.io/train_triangulator/

An interactive spatial triangulation explorer and property-accessibility dataset for unannounced and engineering-study MRT station locations in Singapore, built by fusing public urban planning, transit, procurement, demographic, healthcare, and education datasets.

> **Disclaimer:** Triangulated station coordinates, Bayesian posterior scores, and estimated accessibility gains are statistical spatial estimates derived from public datasets — **not** official Land Transport Authority (LTA) station alignments, government decisions, or financial advice.

---

## Key Coverage (`v3` Multi-Anchor Model)

- **234 Official MRT/LRT Stations** ([official_mrt_stations.csv](official_mrt_stations.csv) / [official_mrt_stations.geojson](official_mrt_stations.geojson)): `146` Operational MRT, `41` Operational LRT, and `47` Announced Future MRT (`TEL5`, `DTL3e`, `JRL`, `CRL1/CPe`, `CRL2`, `NS3A`, `DTL2e DE1/DE2`, `Changi T5`, etc.).
- **34 Triangulated Future Unannounced MRT Stations** ([triangulated_future_mrt_stations.csv](triangulated_future_mrt_stations.csv) / [triangulated_future_mrt_stations.geojson](triangulated_future_mrt_stations.geojson)): Covering `Seletar Line`, `Tengah Line`, `JRL West Coast Extension`, `CRL Phase 3`, independent high-ridership `PV/Bus` rail-gap discoveries, and multi-anchor employment/hospital/education hubs (`>= 700m` heavy-rail gap).
- **339 Benefiting Existing Residential Properties** ([benefiting_properties_postal_codes.csv](benefiting_properties_postal_codes.csv) / [benefiting_properties_postal_codes.geojson](benefiting_properties_postal_codes.geojson)): Verified 6-digit Singapore postal codes across `165` HDB blocks (with 2025–2026 resale medians), `81` Condos/Apartments/ECs, `57` Landed properties, and `36` other residential addresses.
- **99 Unbuilt / Future Sites & Reserve Parcels** ([future_unbuilt_sites_and_parcels.csv](future_unbuilt_sites_and_parcels.csv) / [future_unbuilt_sites_and_parcels.geojson](future_unbuilt_sites_and_parcels.geojson)): 2025–2026 HDB BTO / URA GLS sites plus unbuilt URA Master Plan 2025 Reserve Sites, White Sites, and greenfield parcels.

---

## Integrated Public Data Sources

1. **URA Master Plan 2025 (Oct 2026):** Land-use zoning, Reserve/White Sites, `HEALTH & MEDICAL CARE`, `EDUCATIONAL INSTITUTION`, and job-weighted Commercial / Business Park / Industrial (`B1`/`B2`) GFA across `9,575` parcels.
2. **SingStat General Household Survey 2025 (via `data.gov.sg`):** Official resident population & age groups across all `332` URA subzones (`4.20M` residents) + Planning Area of Workplace employment (`47` areas).
3. **LTA DataMall:** Oct 2026 `PV/Bus` monthly passenger volumes (`240.3M` tap-ins/tap-outs across `5,203` matched bus stops) + AM peak (`07–09h`) directional origins/destinations, full paginated `RoadWorks` (`8,404` records / `721` geocoded `>=365d` persistent roads), and live `TrafficIncidents`.
4. **GeBIZ Government Procurement (`data.gov.sg`):** `718` Land Transport Authority tender awards scanned for engineering studies, site investigations, and tunnel/civil interface works.
5. **Healthcare & Education Anchors (OneMap & MOE):** `59` acute/community/private hospitals and public polyclinics (existing + confirmed `2026–2030s` pipeline), `16` Tertiary/IHL campuses (Universities, Polytechnics, ITEs), and `337` MOE schools.
6. **HDB & OpenStreetMap:** HDB block footprints/postal codes (`13,509` blocks), HDB 2017–Nov 2026 resale transactions, and OSM residential buildings.

---

## Repository Files

| File | Description |
| :--- | :--- |
| [index.html](index.html) / [sg_mrt_triangulator_map.html](sg_mrt_triangulator_map.html) | Self-contained Leaflet WebGIS map with 6 live signal sliders and toggleable anchor overlays |
| [official_mrt_stations.csv](official_mrt_stations.csv) / [official_mrt_stations.geojson](official_mrt_stations.geojson) | Operational MRT/LRT and officially announced future MRT baseline (`234` stations) |
| [triangulated_future_mrt_stations.csv](triangulated_future_mrt_stations.csv) / [triangulated_future_mrt_stations.geojson](triangulated_future_mrt_stations.geojson) | `34` triangulated future MRT stations with Bayesian posteriors and anchor metrics |
| [benefiting_properties_postal_codes.csv](benefiting_properties_postal_codes.csv) / [benefiting_properties_postal_codes.geojson](benefiting_properties_postal_codes.geojson) | `339` top benefiting properties with verified 6-digit postal codes and estimated MRT gap reductions |
| [future_unbuilt_sites_and_parcels.csv](future_unbuilt_sites_and_parcels.csv) / [future_unbuilt_sites_and_parcels.geojson](future_unbuilt_sites_and_parcels.geojson) | `99` upcoming BTO/GLS launches and URA MP2025 unbuilt parcels with reference postcodes |
