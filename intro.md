---
nav_order: 1
---

# Introduction

The JTS Topology Suite is an API for processing linear geometry on the 2-dimensional Cartesian plane. It provides a complete and flexible set of classes for representing and manipulating 0, 1 and 2-dimensional linear geometry. 2-D linear geometry is used in many application areas, including:

* Geographic Information Systems & Geomatics
* Computational Geometry
* CAD/CAM
* Robotics
* Computer Typography
* Computer Games

The theory and algorithms underlying JTS are drawn primarily from the well-researched field of computational geometry (CG). Computational Geometry is a deep, complex field, and much of the research is not easily accessible to the casual user. While it is possible to find implementations of the common algorithms, often they are not written against a complete, functional geometric model.
JTS serves as an accessible, easy to understand repository of many common 
computational geometric algorithsm and concepts, all implemented using a common geometry model.

The design of JTS has the following goals:

* **Robust** - wherever possible provide fully robust, accurate algorithsm, and if robustness failures occur report them to the user in a way that allows for either manual or automated recovery
* Support for explicit, user-definable **precision models**
* **Clear, concise, efficient implementations** of standard computational geometry algorithms.
* **Production-quality** code
* **Tested** - A high-quality set of unit tests for the algorithms and geometric operations. Due to the inherent complexity of geometry, this is a necessity to have any confidence that a geometric API meets its contracts.
* The JTS API provides numerous operations for manipulating and processing geometric objects. It also exposes the fundamental algorithms and data structures that are used to implement the geometric operations. These algorithms and data structures can form the building blocks of numerous other spatial algorithms.
* **Open Source** - because the code is open source, JTS can serve as a model for designing and implementing further spatial algorithms.

JTS has been embedded in many different kinds of software, including:

* GIS applications (JUMP, UDig, Bulgarian thing TMS?)
* Web-Based Mapping frameworks (IMF)
* Spatial Databases (PostGIS)
* Spatial Web Services (GeoServer, deegree)
* Geomatics Application (JCS Conflation Suite, RoadMatcher, RR Skeletonizer)

JTS has been ported to other languages:

* C++ (as GEOS) 
* C# (as NTS)
* Javascript (JSTS)

The GEOS C/C++ library has bindings in many languages, including:

* Python
* R
* Swift

GEOS is used in many applications, including:

* PostGIS
* GDAL
