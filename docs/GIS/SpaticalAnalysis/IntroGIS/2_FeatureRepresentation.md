# 2.Feature Representation
## Vector vs. Raster

### Vector
Vector features can be decomposed into three different geometric primitives: **points**, **polylines** and **polygons**.
#### Point
WKT:`POINT(9 8)`  

1. Points are the most basic geometric primitives having no length or area.  

2. By definition a point can’t be “seen” since it has no area; but this is not practical if such primitives are to be mapped. So points on a map are represented using symbols that have both area and shape (e.g. circle, square, plus signs).

#### Polyline
WKT:`LINESTRING(1 2,2 3,3 1)`

1. A polyline is composed of a sequence of two or more coordinate pairs called vertices (like points).

2. Like a point, a true line can’t be seen since it has no area. And like a point, a line is symbolized using shapes that have a color, width and style (e.g. solid, dashed, dotted, etc…).

#### Polygon
WKT:`POLYGON( (1 2,2 3,3 1,1 2) )`
1. A polygon is composed of three or more line segments whose **starting** and **ending** coordinate pairs are the **same**.

2. Polygons represent both length (i.e. the perimeter of the area) and area.

3. They also embody the idea of an inside and an outside.

### Raster 

1. A raster data model uses an array of cells, or pixels, to represent real-world objects.

2. Implicit in a raster data model is a value associated with each cell or pixel. (This is in contrast to a vector model that may or may not have a value associated with the geometric primitive.)

3. Also note that a raster data structure is square or rectangular. So, if the features in a raster do not cover the full square or rectangular extent, their pixel values will be set to no data values (e.g. `NULL` or `NoData`).

## Object vs. Field

!!! note "Example"
	If we’re interested in studying the distribution of buildings over a study area, then an object view of the features makes sense. 
	If, on the other hand, we are interested in identifying all locations where buildings don’t exist, then a binary field view of these entities would make sense.

### Object View
An object view of the world treats entities as discrete objects; they need not occur at every location within a study area.
### Field View
A field view of the world treats entities as a scalar field. This is a mathematical concept in which a scalar is a quantity having a magnitude. It is measurable at every location within the study region (a property that can be measured at any location).

## Scale
Using Boston region for example

In small scale:

	Boston and other cities -> Point
	Roads -> Polyline

In large scale:

	Boston -> Polygon
	Roads -> Polygon

## Attribute Tables
Non-spatial information associated with a spatial feature is referred to as an **attribute**. Attribute Tables store them.
>A feature on a GIS map is linked to its record in the attribute table by a unique numerical identifier (ID). Every feature in a layer has an identifier.
**Attribute Tables can be combined with Spatial Data Model**
1. It is important to understand the one-to-one or many-to-one relationship between feature, and attribute record. Because features on the map are linked to their records in the table, many GIS software will allow you to click on a map feature and see its related attributes in the table.
2. Raster data can also have attributes only if pixels are represented using a small set of unique integer values. Raster datasets that contain attribute tables typically have cell values that represent or define a class, group, category, or membership.

## Measurement Levels

!!! warning "Title"
	This content is important.  
	It's a key point in Cartography.

Attribute data can be broken down into four **measurement levels**:

- **Nominal** data which have no implied order, size or quantitative information (e.g. paved and unpaved roads).

- **Ordinal** data have an implied order (e.g. ranked scores), however, we cannot quantify the difference since a linear scale is not implied.

- **Interval** data are numeric and have a linear scale, however they do not have a true zero and can therefore not be used to measure _relative_ magnitudes. For example, one cannot say that 60°F is twice as warm as 30°F since when presented in degrees °C the temperature values are 15.5°C and -1.1°C respectively (and 15.5 is clearly not twice as big as -1.1).

- **Ratio** scale data are interval data with a true zero such as monetary value (e.g. $1, $20, $100).
