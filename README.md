### osm2spatialite ###

### Warning: This software is unmaintained ###

This repository contains python script as well as and OSX GUI app for converting .osm or .osm.pbf files into a SpatiaLite format suitable from use by Maps4Mac, which is mostly identical the official PostGIS format.

* Because SpatialLite has no wildcard geometry type world_roads is populated with GEOMETRYCOLLECTION objects, for mapnik to understand these they need to be cast to polygons or linestrings.
* The world_roads and world_polygon tables have a column called osm_type so that the original osm_id can be stored for relations, therefor osm_id is not guaranteed to be unique in these tables. 