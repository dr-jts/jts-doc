---
parent: Input and Output
---

# Well-Known Text (WKT)

Well-Known Text format (WKT) provides a human-readable way of displaying and describing JTS geometry objects.
Syntax Specification
The following syntax specification describes the version of Well-Known Text supported by JTS. 
The specification uses a syntax language similar to that used in the C and Java language specifications.

```
WKTGeometry: one of
        WKTPoint  WKTLineString  WKTLinearRing  WKTPolygon
        WKTMultiPoint  WKTMultiLineString  WKTMultiPolygon
        WKTGeometryCollection

WKTPoint: POINT ( Coordinate )

WKTLineString: LINESTRING CoordinateSequence

WKTLinearRing: LINEARRING CoordinateSequence

WKTPolygon: POLYGON CoordinateSequenceList

WKTMultiPoint: MULTIPOINT CoordinateSequence

WKTMultiLineString: MULTILINESTRING CoordinateSequenceList

WKTMultiPolygon:
        MULTIPOLYGON ( CoordinateSequenceList { , CoordinateSequenceList } )

WKTGeometryCollection: 
        GEOMETRYCOLLECTION ( WKTGeometry { , WKTGeometry } )

CoordinateSequenceList:
	( CoordinateSequence { , CoordinateSequence } )

CoordinateSequence:
	( Coordinate { , Coordinate } )

Coordinate:
	Number Number Numberopt

Number: A Java-style floating-point number
```
