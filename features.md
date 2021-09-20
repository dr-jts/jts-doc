A description of the features and functions provided by
JTS, linked to the relevant
[Javadoc](javadoc/index.html)
for the current version.
<p>

## Geometry Model


* Support for all
[](javadoc/org/locationtech/jts/geom/Geometry.html)Geometry
types defined in the OGC **Simple Features for SQL** specification,
including:


* [](javadoc/org/locationtech/jts/geom/Point.html)Point
and [](javadoc/org/locationtech/jts/geom/MultiPoint.html)MultiPoint
* [](javadoc/org/locationtech/jts/geom/LineString.html)LineString
and [](javadoc/org/locationtech/jts/geom/MultiLineString.html)MultiLineString
* [](javadoc/org/locationtech/jts/geom/Polygon.html)Polygon
and [](javadoc/org/locationtech/jts/geom/MultiPolygon.html)MultiPolygon
* heterogeneous
[](javadoc/org/locationtech/jts/geom/GeometryCollection.html)GeometryCollection




## Geometry Operations


* Topological [](javadoc/org/locationtech/jts/geom/Geometry.html#isValid())validity checking

* [](javadoc/org/locationtech/jts/geom/Geometry.html#getArea())Area
and
[](javadoc/org/locationtech/jts/geom/Geometry.html#getLength())Length/Perimeter

* [](javadoc/org/locationtech/jts/geom/Geometry.html#distance(org.locationtech.jts.geom.Geometry))
Distance between geometries
and
[](javadoc/org/locationtech/jts/geom/Geometry.html#isWithinDistance(org.locationtech.jts.geom.Geometry,%20double))
isWithinDistance predicate

* Spatial Predicates based on the Egenhofer DE-9IM model,
including the named predicates:

* [](javadoc/org/locationtech/jts/geom/Geometry.html#contains(org.locationtech.jts.geom.Geometry))
contains,
[](javadoc/org/locationtech/jts/geom/Geometry.html#within(org.locationtech.jts.geom.Geometry))
within

* [](javadoc/org/locationtech/jts/geom/Geometry.html#covers(org.locationtech.jts.geom.Geometry))
covers,
[](javadoc/org/locationtech/jts/geom/Geometry.html#coveredBy(org.locationtech.jts.geom.Geometry))
coveredBy

* [](javadoc/org/locationtech/jts/geom/Geometry.html#intersects(org.locationtech.jts.geom.Geometry))
intersects,
[](javadoc/org/locationtech/jts/geom/Geometry.html#disjoint(org.locationtech.jts.geom.Geometry))
disjoint

* [](javadoc/org/locationtech/jts/geom/Geometry.html#crosses(org.locationtech.jts.geom.Geometry))
crosses

* [](javadoc/org/locationtech/jts/geom/Geometry.html#overlaps(org.locationtech.jts.geom.Geometry))
overlaps

* [](javadoc/org/locationtech/jts/geom/Geometry.html#touches(org.locationtech.jts.geom.Geometry))
touches

* [](javadoc/org/locationtech/jts/geom/Geometry.html#equals(org.locationtech.jts.geom.Geometry))
equals


and the general
[](javadoc/org/locationtech/jts/geom/Geometry.html#relate(org.locationtech.jts.geom.Geometry))
relate operation returning the DE-9IM
[](javadoc/org/locationtech/jts/geom/IntersectionMatrix.html)
intersection matrix.

* Overlay functions including

* [](javadoc/org/locationtech/jts/geom/Geometry.html#intersection(org.locationtech.jts.geom.Geometry))
intersection,
* [](javadoc/org/locationtech/jts/geom/Geometry.html#difference(org.locationtech.jts.geom.Geometry))
difference,
* [](javadoc/org/locationtech/jts/geom/Geometry.html#union(org.locationtech.jts.geom.Geometry))
union,
* [](javadoc/org/locationtech/jts/geom/Geometry.html#symDifference(org.locationtech.jts.geom.Geometry))
symmetric difference
* [](javadoc/org/locationtech/jts/geom/Geometry.html#union())
unary union, providing fast union of geometry collections


* [](javadoc/org/locationtech/jts/geom/Geometry.html#buffer(double))
Buffer computation (also known as Minkowski sum with a circle)

* selection of different
[](javadoc/org/locationtech/jts/geom/Geometry.html#buffer(double,%20int,%20int))end-cap and join
styles.


* [](javadoc/org/locationtech/jts/geom/Geometry.html#convexHull())Convex hull
* [](javadoc/org/locationtech/jts/simplify/package-summary.html)Geometric simplification
including the
[](javadoc/org/locationtech/jts/simplify/DouglasPeuckerSimplifier.html)
Douglas-Peucker algorithm
and
[](javadoc/org/locationtech/jts/simplify/TopologyPreservingSimplifier.html)
topology-preserving simplification
* Geometric [](javadoc/org/locationtech/jts/densify/Densifier.html)densification
* [](javadoc/org/locationtech/jts/linearref/package-summary.html)Linear referencing


## Precision Handling

* Explicit coordinate
[](javadoc/org/locationtech/jts/geom/PrecisionModel.html)Precision Model
* Geometry precision reduction


## Geometric Constructions

* [](javadoc/org/locationtech/jts/triangulate/DelaunayTriangulationBuilder.html)
Delaunay triangulation
and
[](javadoc/org/locationtech/jts/triangulate/ConformingDelaunayTriangulationBuilder.html)
Conforming Delaunay triangulation
* [](javadoc/org/locationtech/jts/triangulate/VoronoiDiagramBuilder.html)
Voronoi diagram generation
* [](javadoc/org/locationtech/jts/algorithm/MinimumDiameter.html)
Minimum Diameter
of a geometry
* [](javadoc/org/locationtech/jts/algorithm/MinimumDiameter.html#getMinimumRectangle())
Minimum Enclosing Rectangle
* [](javadoc/org/locationtech/jts/algorithm/MinimumBoundingCircle.html)
Minimum Bounding Circle


## Metric Functions

* [](javadoc/org/locationtech/jts/operation/distance/DistanceOp.html)Distance between geometries, with supporting points
* [](javadoc/org/locationtech/jts/algorithm/distance/DiscreteHausdorffDistance.html)
Discrete Hausdorff distance
* [](javadoc/org/locationtech/jts/algorithm/match/AreaSimilarityMeasure.html)Area and
[](javadoc/org/locationtech/jts/algorithm/match/HausdorffSimilarityMeasure.html)Hausdorff<a>
similarity measures


## Spatial algorithms

* [](javadoc/org/locationtech/jts/algorithm/RobustLineIntersector.html)Robust line segment intersection
* Efficient line arrangement
[](javadoc/org/locationtech/jts/noding/package-summary.html)intersection and noding
* [](javadoc/org/locationtech/jts/noding/snapround/package-summary.html)
Snap-rounding for noding line arrangements
* Efficient [](javadoc/org/locationtech/jts/algorithm/locate/package-summary.html)Point-in-Polygon testing


## Mathematical Functions

* [](javadoc/org/locationtech/jts/algorithm/Angle.html)Angle computation
* [](javadoc/org/locationtech/jts/algorithm/VectorMath.html)Vector arithmetic


## Spatial structures

* Spatial index structures including:

* [](javadoc/org/locationtech/jts/index/quadtree/Quadtree.html)Quadtree
* [](javadoc/org/locationtech/jts/index/strtree/STRtree.html)STR-tree
* [](javadoc/org/locationtech/jts/index/kdtree/KdTree.html)KD-tree
* [](javadoc/org/locationtech/jts/index/intervalrtree/package-summary.html)Interval R-tree
* [](javadoc/org/locationtech/jts/index/chain/package-summary.html)Monotone Chains

* [](javadoc/org/locationtech/jts/planargraph/PlanarGraph.html)Planar graphs
and [](javadoc/org/locationtech/jts/planargraph/algorithm/package-summary.html)graph algorithms


## Input/Output

* WKT (Well-Known Text)
[](javadoc/org/locationtech/jts/io/WKTReader.html)reading and
[](javadoc/org/locationtech/jts/io/WKTWriter.html)writing
* WKB (Well-Known Binary)
[](javadoc/org/locationtech/jts/io/WKBReader.html)reading
and
[](javadoc/org/locationtech/jts/io/WKBWriter.html)writing
* GML(Geography Markup Language) Version 2
[](javadoc/org/locationtech/jts/io/gml2/GMLReader.html)reading
and
[](javadoc/org/locationtech/jts/io/gml2/GMLWriter.html)writing
* Java Swing/AWT Shape [](javadoc/org/locationtech/jts/awt/package-summary.html)writing


## High-Precision Arithmetic

* [](javadoc/org/locationtech/jts/algorithm/RobustDeterminant.html)
Robust evaluation of 2x2 double-precision determinants
* [](javadoc/org/locationtech/jts/math/DD.html)
DoubleDouble extended-precision arithmetic
