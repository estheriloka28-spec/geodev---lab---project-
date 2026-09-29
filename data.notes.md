# Data notes 

## NGA LGA Boundaries (GRID3)
- Source: https://data.grid3.org
- Downloaded: 27/09/2026
- Features: 774 features, polygons (All Nigeria LGAs)
- Columns: FID (integer), globalid (text), uniq_id (text), timestamp (date), editor (text), lganame (text), lgacode (text), statename (text), statecode (text), source (text), amapcode (text)
- No nulls in lganame, statename
- Geometry type: Polygon (MultiPolygon)
- Coverage: Covers all 774 LGAs in Nigeria. Oshodi-Isolo extracted. 

## OSM roads, extracted via QuickOSM
- Source: OpenStreetMap via QuickOSM plugin in QGIS
- Query: Key=highway, Value=* within oshodi_boundary extent
- Extracted: 27/09/2026
- Features: 2,626 features, lines
- Many nulls in name and surface - paved/unpaved cannot be separated everywhere.
- Coverage: Good in built-up area, gaps are airport and large compounds. 
## CRS and preparation
- All source layers arrived in EPSG:4326
- Study area: Oshodi-Isolo LGA, extracted from GRID3 Nigeria LGA Boundaries
- All layers clipped to study area, then reprojected to EPSG:32631 (UTM 31N)
- Area check: Oshodi-Isolo 54.04 km2, matches published figure (45-50 km2 range) - sanity check PASS
- Working files in data/processed/, raw files untouched in data/raw/
