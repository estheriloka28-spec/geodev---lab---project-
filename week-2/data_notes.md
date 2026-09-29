# Data notes 

## NGA LGA Boundaries (GRID3)
- Source: https://data.grid3.org
- Downloaded: 27/09/2026
- Features: 774 features, polygons (All Nigeria LGAs)
- Columns: FID (integer), globalid (text), uniq_id (text), timestamp (date), editor (text), lganame (text), lgacode (text), statename (text), statecode (text), source (text), amapcode (text)
- No nulls in lganame, statename
- Geometry type: Polygon (MultiPolygon)
- Coverage: Covers all 774 LGAs in Nigeria. Oshodi-Isolo extracted.

## Waterways
- Source: HOTOSM via HDX
- Source Link: https://production-raw-data-api.s3.amazonaws.com/ISO3/NGA/waterways/hotosm_nga_waterways_osm_shp.zip
-Downloaded 28/09/2026
- Features:
- Columns

## Dumpsites
- Source: eHealth Africa GeoServer - sv_dump_sites
- Source Link: https://gis-geoserver.ehealthafrica.org/geoserver/eHA_db/ows?service=WFS&version=1.0.0&request=GetFeature&typeName=eHA_db:sv_dump_sites&outputFormat=application/json&authkey=fdfe9a37-d2d8-4210-9a15-25dab5d907fa
- Downloaded 28/09/2026
- Note: Only 1 feature returned for Oshodi-Isolo after clipping - major data gap identified.
  
## LAWMA Official (Custom Excel)
- Method: Manual Excel compilation, lat/long -> Point
- 6 features
- Columns: Name, latitude, longitude, type
- Finding: 0 of 6 fall inside Oshodi-Isolo LGA

## Land use - Landfill (OSM Supplement)
- Source: QuickOSM search - key=landuse, value=landfill
- Geometry: MultiPolygon
- Features: 1 in Lagos

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
