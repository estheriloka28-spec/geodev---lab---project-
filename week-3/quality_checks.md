# Week 3 - Data Preparation & Quality Checks
Study Area: Oshodi-Isolo LGA, Lagos, Nigeria

## 1. Prepared Dataset: prepared-data.csv
- Source: Primary mapping in QGIS - 10 informal dumpsites identified via satellite + local knowledge
- File: `dumpsites_wgs84` exported to CSV
- Columns: fid, Name, lat (EPSG:4326), lon (EPSG:4326)
- CRS: Original digitized in EPSG:32631 (UTM Zone 31N) for accurate distance/buffer analysis, then reprojected to EPSG:4326 for standard lat/lon

## 2. Quality Checks (5 dimensions)
### Completeness:
- 10/10 points have names - no NULL values. Fixed from initial NULLs.
- All 10 points within Oshodi-Isolo boundary after clipping.
### Positional Accuracy:
- Initial error: lat = 7, lon = 3 (placeholder). Fixed by re-exporting from UTM layer.
- Final accuracy: lat 6.497 - 6.559, lon 3.290 - 3.339 - all within Lagos State bounds.
### Attribute Accuracy:
- Names standardized: Ago_Palace, Bucknor_Estate, Oshodi_Bolade, Egbe_Ikotun, Isolo_Centre, Cele_Okota, Ajao_Estate, Ejigbo_North, Hasangah, Mafoluku.
- Each name corresponds to community/landmark in Oshodi-Isolo.
### Fitness for Purpose:
- Fit for Week 4 analysis: Buffer (500m), proximity to waterways/roads, and vulnerability mapping.
## 3. Files in week-3/
- prepared-data.csv: Final 10 points with correct WGS84 coordinates
- quality_checks.md: This file
