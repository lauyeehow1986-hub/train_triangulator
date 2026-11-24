# Singapore Future MRT Station Triangulator & 10-Yr Property ROI WebGIS (`v4`)

**Live Interactive WebGIS:** https://lauyeehow1986-hub.github.io/train_triangulator/

An interactive spatial triangulation explorer and 10-year Monte Carlo property investment simulator for unannounced and engineering-study MRT station locations in Singapore, built by fusing public urban planning, transit, procurement, demographic, healthcare, education, and 2017–2026 residential transaction datasets (default OpenStreetMap basemap with a dedicated **Invest / ROI** tab).

> **Disclaimer:** Triangulated station coordinates, Bayesian posterior scores, and 10-year Monte Carlo property gain simulations are statistical spatial estimates derived from public datasets — **not** official Land Transport Authority (LTA) station alignments, government decisions, or financial advice.

---

## Key Coverage (`v4` Multi-Anchor + 10Y Monte Carlo ROI)

- **234 Official MRT/LRT Stations** ([official_mrt_stations.csv](official_mrt_stations.csv) / [official_mrt_stations.geojson](official_mrt_stations.geojson)): `146` Operational MRT, `41` Operational LRT, and `47` Announced Future MRT (`TEL5`, `DTL3e`, `JRL`, `CRL1/CPe`, `CRL2`, `NS3A`, `DTL2e DE1/DE2`, `Changi T5`, etc.).
- **34 Triangulated Future Unannounced MRT Stations** ([triangulated_future_mrt_stations.csv](triangulated_future_mrt_stations.csv) / [triangulated_future_mrt_stations.geojson](triangulated_future_mrt_stations.geojson)): Covering `Seletar Line`, `Tengah Line`, `JRL West Coast Extension`, `CRL Phase 3`, independent high-ridership `PV/Bus` rail-gap discoveries, and multi-anchor employment/hospital/education hubs (`>= 700m` heavy-rail gap).
- **339 Benefiting Existing Residential Properties & 10-Yr MC Simulation** ([property_investment_simulation_postcodes.csv](property_investment_simulation_postcodes.csv) / [benefiting_properties_postal_codes.csv](benefiting_properties_postal_codes.csv)): `2,000`-trial 10-year Monte Carlo simulation calibrated on `245,441` HDB resale transactions (`2017-01` to `2026-11`), SingStat 2017–2026 Property Price Indices, and Data.gov.sg HDB median rents (`2026-Q3`), reporting expected 10-yr gains, P10–P90 bands, lease decay, and levered annual ROI (SC 1st & SC 2nd `20%` ABSD).
- **34 Station Area Summaries & 7 2025–2026 BTO Launches** ([station_area_investment_summary.csv](station_area_investment_summary.csv)): Area-level risk-adjusted 10-year gains alongside 5-yr MOP Standard (`0%` clawback) vs 10-yr MOP Prime (`14%` clawback) 4-room BTO exit projections.
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
| [index.html](index.html) / [sg_mrt_triangulator_map.html](sg_mrt_triangulator_map.html) | Self-contained OpenStreetMap-default Leaflet WebGIS map with 6 live signal sliders, anchor overlays, and dedicated **Invest / ROI** tab |
| [property_investment_simulation_postcodes.csv](property_investment_simulation_postcodes.csv) | `2,000`-trial 10-year Monte Carlo forecasts across all `339` verified postal codes (gains, P10–P90 bands, SC 1st/2nd ABSD ROIs, lease decay, rankings) |
| [station_area_investment_summary.csv](station_area_investment_summary.csv) | Risk-adjusted 10-year gain summaries for all `34` triangulated station areas and `7` 2025–2026 BTO launches |
| [official_mrt_stations.csv](official_mrt_stations.csv) / [official_mrt_stations.geojson](official_mrt_stations.geojson) | Operational MRT/LRT and officially announced future MRT baseline (`234` stations) |
| [triangulated_future_mrt_stations.csv](triangulated_future_mrt_stations.csv) / [triangulated_future_mrt_stations.geojson](triangulated_future_mrt_stations.geojson) | `34` triangulated future MRT stations with Bayesian posteriors and anchor metrics |
| [benefiting_properties_postal_codes.csv](benefiting_properties_postal_codes.csv) / [benefiting_properties_postal_codes.geojson](benefiting_properties_postal_codes.geojson) | `339` top benefiting properties with verified 6-digit postal codes and estimated MRT gap reductions |
| [future_unbuilt_sites_and_parcels.csv](future_unbuilt_sites_and_parcels.csv) / [future_unbuilt_sites_and_parcels.geojson](future_unbuilt_sites_and_parcels.geojson) | `99` upcoming BTO/GLS launches and URA MP2025 unbuilt parcels with reference postcodes |
