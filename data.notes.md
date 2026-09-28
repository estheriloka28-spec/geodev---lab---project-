# Data notes 

## NGA LGA Boundaries (GRID3)
- Source: NGA_LGA_Boundaries shapefile / geojson
- Downloaded: 27/09/2026
- Features: 774 features, polygons (All Nigeria LGAs)
- Columns: FID (integer), globalid (text), uniq_id (text), timestamp (date), editor (text), lganame (text), lgacode (text), statename (text), statecode (text), source (text), amapcode (text)
- No nulls in lganame, statename
- Geometry type: Polygon (MultiPolygon)
- Coverage: Covers all 774 LGAs in Nigeria. Oshodi-Isolo extracted as oshodi_boundary.geojson. 

## OSM roads, extracted via QuickOSM
- Source: OpenStreetMap via QuickOSM plugin in QGIS
- Query: Key=highway, Value=* within oshodi_boundary extent
- Extracted: 27/09/2026
- Features: 2,626 features, lines
- Many nulls in name and surface - paved/unpaved cannot be separated everywhere.
- Coverage: Good in built-up area, gaps are airport and large compounds. 
