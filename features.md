# JTS Feature Summary
{: .no_toc }

A description of the features and functions provided by
JTS, with links to the
[Javadoc](https://locationtech.github.io/jts/javadoc/index.html).

1. TOC
{:toc}


## Geometry Model

Support for all geometry types defined in the OGC *Simple Features for SQL* specification,
including:

* [Geometry](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html) (abstract base class)
* [Point](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Point.html)
* [LineString](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/LineString.html)
* [Polygon](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Polygon.html)
* [MultiPoint](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/MultiPoint.html)
* [MultiLineString](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/MultiLineString.html)
* [MultiPolygon](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/MultiPolygon.html)
* heterogeneous [GeometryCollection](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/GeometryCollection.html)

## Geometry I/O

* WKT (Well-Known Text)
  [reader](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/io/WKTReader.html)
  and [writer](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/io/WKTWriter.html)
* WKB (Well-Known Binary)
  [reader](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/io/WKBReader.html)
  and [writer](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/io/WKBWriter.html)
* GML(Geography Markup Language) Version 2
  [reader](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/io/gml2/GMLReader.html)
  and [writer](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/io/gml2/GMLWriter.html)
* Java Swing/AWT Shape [writer](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/awt/package-summary.html)

## Validation and Repair

* Topological [validity checking](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#isValid())

## Geometry Operations

* [Area](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#getArea())
* [Length/Perimeter](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#getLength())
* [Distance between geometries](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#distance(org.locationtech.jts.geom.Geometry))
and
[isWithinDistance](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#isWithinDistance(org.locationtech.jts.geom.Geometry,%20double))
 predicate
* Spatial Predicates based on the Egenhofer DE-9IM model, including the named predicates:
  * [contains](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#contains(org.locationtech.jts.geom.Geometry)),
    [within](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#within(org.locationtech.jts.geom.Geometry))
  * [covers](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#covers(org.locationtech.jts.geom.Geometry)),
    [coveredBy](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#coveredBy(org.locationtech.jts.geom.Geometry))
  * [intersects](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#intersects(org.locationtech.jts.geom.Geometry)),
    [disjoint](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#disjoint(org.locationtech.jts.geom.Geometry))
  * [crosses](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#crosses(org.locationtech.jts.geom.Geometry))
  * [overlaps](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#overlaps(org.locationtech.jts.geom.Geometry))
  * [touches](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#touches(org.locationtech.jts.geom.Geometry))
  * [equals](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#equals(org.locationtech.jts.geom.Geometry))
and the general
[relate](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#relate(org.locationtech.jts.geom.Geometry))
 predicate returning the DE-9IM
[intersection matrix](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/IntersectionMatrix.html)

* Overlay functions including

  * [intersection](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#intersection(org.locationtech.jts.geom.Geometry))
  * [difference](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#difference(org.locationtech.jts.geom.Geometry))
  * [symmetric difference](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#symDifference(org.locationtech.jts.geom.Geometry))
  * [union](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#union(org.locationtech.jts.geom.Geometry))
  * [unary union](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#union()), providing fast union of geometry collections

* [Buffer](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#buffer(double))
  computation (also known as Minkowski sum with a circle)
  * selection of buffer [end-cap and join styles](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#buffer(double,%20int,%20int)).

* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/Geometry.html#convexHull())Convex hull
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/simplify/package-summary.html)Geometric simplification
including the
[](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/simplify/DouglasPeuckerSimplifier.html)
Douglas-Peucker algorithm
and
[](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/simplify/TopologyPreservingSimplifier.html)
topology-preserving simplification
* Geometric [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/densify/Densifier.html)densification
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/linearref/package-summary.html)Linear referencing


## Precision Handling

* Explicit coordinate
[](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/geom/PrecisionModel.html)Precision Model
* Geometry precision reduction


## Geometric Constructions

* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/triangulate/DelaunayTriangulationBuilder.html)
Delaunay triangulation
and
[](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/triangulate/ConformingDelaunayTriangulationBuilder.html)
Conforming Delaunay triangulation
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/triangulate/VoronoiDiagramBuilder.html)
Voronoi diagram generation
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/MinimumDiameter.html)
Minimum Diameter
of a geometry
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/MinimumDiameter.html#getMinimumRectangle())
Minimum Enclosing Rectangle
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/MinimumBoundingCircle.html)
Minimum Bounding Circle


## Metric Functions

* [Euclidean Distance](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/operation/distance/DistanceOp.html) between geometries, with nearest points
* [Discrete Hausdorff distance](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/distance/DiscreteHausdorffDistance.html), with nearest points
* [Discrete Frechet distance](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/distance/DiscreteFrechetDistance.html), with nearest points
* [Area](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/match/AreaSimilarityMeasure.html) and
[Hausdorff](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/match/HausdorffSimilarityMeasure.html)
similarity measures


## Spatial algorithms

* [Robust line segment intersection](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/RobustLineIntersector.html)
* Efficient line arrangement
[intersection and noding](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/noding/package-summary.html)
* [Snap-rounding](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/noding/snapround/package-summary.html)
 for noding line arrangements
* Efficient [Point-in-Polygon](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/locate/package-summary.html) testing


## Spatial structures

* Spatial index structures including:

* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/index/quadtree/Quadtree.html)Quadtree
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/index/strtree/STRtree.html)STR-tree
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/index/kdtree/KdTree.html)KD-tree
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/index/intervalrtree/package-summary.html)Interval R-tree
* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/index/chain/package-summary.html)Monotone Chains

* [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/planargraph/PlanarGraph.html)Planar graphs
and [](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/planargraph/algorithm/package-summary.html)graph algorithms



## Mathematical Functions

* [Angle](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/Angle.html) computations
* [Vector arithmetic](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/VectorMath.html)


## High-Precision Arithmetic

* [Robust evaluation of 2x2 double-precision determinants](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/algorithm/RobustDeterminant.html)
* [DoubleDouble](https://locationtech.github.io/jts/javadoc/org/locationtech/jts/math/DD.html) extended-precision arithmetic
