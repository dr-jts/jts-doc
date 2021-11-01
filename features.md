# Feature Summary
{: .no_toc }

A description of the features and functions provided by
JTS, with links to the
[Javadoc](javadoc/index.html).

1. TOC
{:toc}


## Geometry Model

* Support for all
geometry
types defined in the OGC *Simple Features for SQL* specification,
including:

* [Geometry](javadoc/org/locationtech/jts/geom/Geometry.html) (abstract base class)
* [Point](javadoc/org/locationtech/jts/geom/Point.html)
* [LineString](javadoc/org/locationtech/jts/geom/LineString.html)
* [Polygon](javadoc/org/locationtech/jts/geom/Polygon.html)
* [MultiPoint](javadoc/org/locationtech/jts/geom/MultiPoint.html)
* [MultiLineString](javadoc/org/locationtech/jts/geom/MultiLineString.html)
* [MultiPolygon](javadoc/org/locationtech/jts/geom/MultiPolygon.html)
* heterogeneous [GeometryCollection](javadoc/org/locationtech/jts/geom/GeometryCollection.html)

## Geometry I/O

* WKT (Well-Known Text)
  [reader](javadoc/org/locationtech/jts/io/WKTReader.html)
  and [writer](javadoc/org/locationtech/jts/io/WKTWriter.html)
* WKB (Well-Known Binary)
  [reader](javadoc/org/locationtech/jts/io/WKBReader.html)
  and [writer](javadoc/org/locationtech/jts/io/WKBWriter.html)
* GML(Geography Markup Language) Version 2
  [reader](javadoc/org/locationtech/jts/io/gml2/GMLReader.html)
  and [writer](javadoc/org/locationtech/jts/io/gml2/GMLWriter.html)
* Java Swing/AWT Shape [writer](javadoc/org/locationtech/jts/awt/package-summary.html)



## Geometry Operations

* Topological [validity checking](javadoc/org/locationtech/jts/geom/Geometry.html#isValid())
* [Area](javadoc/org/locationtech/jts/geom/Geometry.html#getArea())
* [Length/Perimeter](javadoc/org/locationtech/jts/geom/Geometry.html#getLength())
* [Distance between geometries](javadoc/org/locationtech/jts/geom/Geometry.html#distance(org.locationtech.jts.geom.Geometry))
and
[isWithinDistance](javadoc/org/locationtech/jts/geom/Geometry.html#isWithinDistance(org.locationtech.jts.geom.Geometry,%20double))
 predicate
* Spatial Predicates based on the Egenhofer DE-9IM model, including the named predicates:
  * [contains](javadoc/org/locationtech/jts/geom/Geometry.html#contains(org.locationtech.jts.geom.Geometry)),
    [within](javadoc/org/locationtech/jts/geom/Geometry.html#within(org.locationtech.jts.geom.Geometry))
  * [covers](javadoc/org/locationtech/jts/geom/Geometry.html#covers(org.locationtech.jts.geom.Geometry)),
    [coveredBy](javadoc/org/locationtech/jts/geom/Geometry.html#coveredBy(org.locationtech.jts.geom.Geometry))
  * [intersects](javadoc/org/locationtech/jts/geom/Geometry.html#intersects(org.locationtech.jts.geom.Geometry)),
    [disjoint](javadoc/org/locationtech/jts/geom/Geometry.html#disjoint(org.locationtech.jts.geom.Geometry))
  * [crosses](javadoc/org/locationtech/jts/geom/Geometry.html#crosses(org.locationtech.jts.geom.Geometry))
  * [overlaps](javadoc/org/locationtech/jts/geom/Geometry.html#overlaps(org.locationtech.jts.geom.Geometry))
  * [touches](javadoc/org/locationtech/jts/geom/Geometry.html#touches(org.locationtech.jts.geom.Geometry))
  * [equals](javadoc/org/locationtech/jts/geom/Geometry.html#equals(org.locationtech.jts.geom.Geometry))
and the general
[relate](javadoc/org/locationtech/jts/geom/Geometry.html#relate(org.locationtech.jts.geom.Geometry))
 predicate returning the DE-9IM
[intersection matrix](javadoc/org/locationtech/jts/geom/IntersectionMatrix.html)

* Overlay functions including

  * [intersection](javadoc/org/locationtech/jts/geom/Geometry.html#intersection(org.locationtech.jts.geom.Geometry))
  * [difference](javadoc/org/locationtech/jts/geom/Geometry.html#difference(org.locationtech.jts.geom.Geometry))
  * [symmetric difference](javadoc/org/locationtech/jts/geom/Geometry.html#symDifference(org.locationtech.jts.geom.Geometry))
  * [union](javadoc/org/locationtech/jts/geom/Geometry.html#union(org.locationtech.jts.geom.Geometry))
  * [unary union](javadoc/org/locationtech/jts/geom/Geometry.html#union()), providing fast union of geometry collections

* [Buffer](javadoc/org/locationtech/jts/geom/Geometry.html#buffer(double))
  computation (also known as Minkowski sum with a circle)
  * selection of buffer [end-cap and join styles](javadoc/org/locationtech/jts/geom/Geometry.html#buffer(double,%20int,%20int)).

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

* [Euclidean Distance](javadoc/org/locationtech/jts/operation/distance/DistanceOp.html) between geometries, with nearest points
* [Discrete Hausdorff distance](javadoc/org/locationtech/jts/algorithm/distance/DiscreteHausdorffDistance.html), with nearest points
* [Discrete Frechet distance](javadoc/org/locationtech/jts/algorithm/distance/DiscreteFrechetDistance.html), with nearest points
* [Area](javadoc/org/locationtech/jts/algorithm/match/AreaSimilarityMeasure.html) and
[Hausdorff](javadoc/org/locationtech/jts/algorithm/match/HausdorffSimilarityMeasure.html)
similarity measures


## Spatial algorithms

* [Robust line segment intersection](javadoc/org/locationtech/jts/algorithm/RobustLineIntersector.html)
* Efficient line arrangement
[intersection and noding](javadoc/org/locationtech/jts/noding/package-summary.html)
* [Snap-rounding](javadoc/org/locationtech/jts/noding/snapround/package-summary.html)
 for noding line arrangements
* Efficient [Point-in-Polygon](javadoc/org/locationtech/jts/algorithm/locate/package-summary.html) testing


## Spatial structures

* Spatial index structures including:

* [](javadoc/org/locationtech/jts/index/quadtree/Quadtree.html)Quadtree
* [](javadoc/org/locationtech/jts/index/strtree/STRtree.html)STR-tree
* [](javadoc/org/locationtech/jts/index/kdtree/KdTree.html)KD-tree
* [](javadoc/org/locationtech/jts/index/intervalrtree/package-summary.html)Interval R-tree
* [](javadoc/org/locationtech/jts/index/chain/package-summary.html)Monotone Chains

* [](javadoc/org/locationtech/jts/planargraph/PlanarGraph.html)Planar graphs
and [](javadoc/org/locationtech/jts/planargraph/algorithm/package-summary.html)graph algorithms



## Mathematical Functions

* [Angle](javadoc/org/locationtech/jts/algorithm/Angle.html) computations
* [Vector arithmetic](javadoc/org/locationtech/jts/algorithm/VectorMath.html)


## High-Precision Arithmetic

* [Robust evaluation of 2x2 double-precision determinants](javadoc/org/locationtech/jts/algorithm/RobustDeterminant.html)
* [DoubleDouble](javadoc/org/locationtech/jts/math/DD.html) extended-precision arithmetic
