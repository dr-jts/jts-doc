## JTS Design Flaws

In the rush to get JTS out the door, some design decisions were made that in hindsight might not have been the best ones.  

### Invalid Zero-Length Lines

It would be better if zero-length linestrings were considered valid.  This is convenient and logically complete.
It is consistent with the decision to allow repeated points in geometries.
This may have been based on an overly-strict interpretation of the OGC semantics (which should have explicitiy clarified this).
It generally doesn't affect algorithms at all (although algorithms should be designed to avoid emitting zero-length lines whereever possible).
Alternatively this could be handled via providing a notion of "JTS-valid" which is more lenient than OGC validity.

If this is allowed then should zero-area polygons be valid as well?

