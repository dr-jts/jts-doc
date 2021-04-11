---
parent: Input and Output
---

# Well-Known Binary (WKB)

Well-Known Binary format (WKB) provides an efficent, exact means of representing JTS geometry objects. Because the format is binary, it exactly represents floating-point values (unlike WKT, which unavoidably rounds exact floating-point values during conversion to and from the textual representation. WKB is often used as a format for communication between database systems and client software.
The WKB orignally defined in the OGC-SFS supports only 2-dimensional coordinates. Since many systems need to support 3-D coordinates, an extension to WKB has been informally defined as EWKB. It extends the WKB spec to allow representing geometry with 3-D coordinates. Each WKB packet is tagged to indicate whether it contains 2 or 3 dimensional coordinates. JTS supports the EWKB extension.

Syntax Specification
The following syntax specification describes the version of Well-Known Binary supported by JTS. 
The specification uses a language similar to the C type description syntax. 
Note the use of bit-field specifiers to define how the dimension indicator and the geometry type code are stored in the same 32-bit word.

```
Coordinate {
    double x;
    double y;
    [ double z; ]  // only if 3-D
}

CoordinateSeq {
    uint32     numCoords;
    Coordinate pts[numCoords];
}

enum wkbGeometryType {
    wkbPoint              = 1,
    wkbLineString         = 2,
    wkbPolygon            = 3,
    wkbMultiPoint         = 4,
    wkbMultiLineString    = 5,
    wkbMultiPolygon       = 6,
    wkbGeometryCollection = 7
}

enum wkbByteOrder {
    wkbXDR = 0,  // Big Endian
    wkbNDR = 1   // Little Endian
}

enum wkbDimension {
    is2D = 0,  // 2-D coordinates
    is3D = 1   // 3-D coordinates
}

WKBType {
    uint32  dimension : 1;
    uint32  geomType  : 31;
}

WKBGeometry {
    union {
        WKBPoint              point;
        WKBLineString         linestring;
        WKBPolygon            polygon;
        WKBGeometryCollection collection;
        WKBMultiPoint         mpoint;
        WKBMultiLineString    mlinestring;
        WKBMultiPolygon       mpolygon;
} }

WKBPoint {
    byte       byteOrder;
    WKBType    wkbType;  // = 1
    Coordinate point;
}

WKBLineString {
    byte          byteOrder;
    WKBType       wkbType;  // = 2
    CoordinateSeq seq;
}

WKBPolygon {
    byte          byteOrder;
    WKBType       wkbType;  // = 3
    uint32        numItems;
    CoordinateSeq rings[numItems];
}

WKBMultiPoint {
    byte          byteOrder;
    WKBType       wkbType;  // = 4
    CoordinateSeq seq;
}

WKBMultiLineString {
    byte          byteOrder;
    WKBType       wkbType;  // = 5
    uint32        numItems;
    WKBLineString wkbLineStrings[numItems];
}

WKBMultiPolygon {
    byte       byteOrder;
    WKBType    wkbType;  // = 6
    uint32     numItems;
    WKBPolygon wkbPolygons[numItems];
}

WKBGeometryCollection {
    byte        byteOrder;
    WKBType     wkbType;  // = 7
    uint32      numItems;
    WKBGeometry wkbGeometries[numItems];
}
```
