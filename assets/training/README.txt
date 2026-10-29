ATLAS SYNTHETIC TRAINING DATA / بيانات تدريب افتراضية

These coordinates and names are fictional educational examples, not a survey,
real facility inventory, or authoritative representation of Makkah.

CAD: training-campus.dxf is ASCII R12 DXF. Its coordinate numbers are meters in
WGS 84 / UTM zone 37N, EPSG:32637. Keep training-campus.prj beside it with the
same base filename. The older DXF format does not itself define the GIS CRS.

Layers: BUILDINGS has 3 closed POLYLINE entities, GATES has 2 POINT entities,
ROADS has 2 LINE entities. CAD reading can expose geometry in multiple classes;
filter by layer and geometry and inspect results before counting assets.

The CAD entities contain geometry and layer names, not business identifiers.
Use asset-register.csv with documented bounding coordinates to verify identity
before populating fields. Do not join by row order or OBJECTID.

GeoJSON: buildings.geojson, gates.geojson, roads.geojson use WGS 84 longitude,
latitude per GeoJSON convention, transformed from the same UTM coordinates.
In ArcGIS Pro use JSON To Features or supported input workflows. In QGIS use
Add Vector Layer. PROJECT to EPSG:32637 for planar metric analysis; do not
assign a UTM definition to longitude/latitude numbers.

Oracle: G01 = (582000,2366000). A planar 100 m buffer intersecting footprints
returns B01 and B02. B03 is outside. This is straight-line distance, not walking
distance. The accompanying website diagram is conceptual, not to scale.

test-cases.csv is a blank execution record. Fill Actual and Evidence only after
running the tests. data-dictionary.csv provides a starter attribute dictionary.

Suggested workflow: inspect source > validate CRS > CAD To Geodatabase > filter
by Layer and geometry > export working feature classes > populate attributes >
validate > buffer/intersect > export layout > execute tests and package sources.
