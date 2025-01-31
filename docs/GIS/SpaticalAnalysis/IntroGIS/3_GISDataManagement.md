## Intro
Subset of spatial data file formats(this course focus on)
1. shapefiles -> vector data
2. imagine and GeoTiff -> rasters
3. file geodatabases and geopackages -> both vector and raster data

## Vector Data file formats
### Shapefile
1. Conceptually, a shapefile is a feature class–it stores a collection of features that have the same geometry type (point, line, or polygon), the same attributes, and a common spatial extent.
2. Despite what its name may imply, a “single” shapefile is actually composed of at least ==three== files, and as many as ==eight==1. Each file that makes up a “shapefile” has a common filename but different extension types.

| File extension |            Content            |
| :------------: | :---------------------------: |
|      .dbf      |     Attribute information     |
|      .shp      |       Feature geometry        |
|      .shx      |    Feature geometry index     |
|      .aih      |        Attribute index        |
|      .ain      |        Attribute index        |
|      .prj      | Coordinate system information |
|      .sbn      |      Spatial index file       |
|      .sbx      |      Spatial index file       |

### File Geodatabase
1. A **file geodatabase** is a relational database storage format. 
2. It’s a far more complex data structure than the shapefile and consists of a **.gdb** folder housing dozens of files.

### GeoPackage
1. This is a relatively new data format that follows [open format standards](https://en.wikipedia.org/wiki/Open_format) (i.e. it is non-proprietary). It’s built on top of SQLite (a self-contained relational database).
2. Its filename usually ends in `.gpkg`.

## Raster Data file formats
### Imagine
1. This file format consists of a single **.img** file.
2. It is sometimes accompanied by an .xml file which usually stores metadata information about the raster layer.

### GeoTiff
If maximum portability and platform independence is important, this file format may be a good choice.

### File Geodatabase
1. Geodatabases have the benefit of defining image mosaic structures thus allowing the user to create “stitched” images from multiple image files stored in the geodatabase.
2. Also, processing very large raster files can be computationally more efficient when stored in a file geodatabase as opposed to an Imagine or GeoTiff file format.
