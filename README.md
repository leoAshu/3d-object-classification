# 3D Object Classification

## OFF File:

- stands for Object File Format
- is a geometry definition file format containing the description of the composing polygons of a geometric object
- can store 2D or 3D objects
- originally developed for [Geomview](http://www.geomview.org/), a geometry visualization software


### Composition of an OFF File:

- First line:
    - optional
    - the letters `OFF` to mark the file type

- Second line:
    - a 3 value tuple: `(#vertices, #faces, #edges)`
    - edges can be ignored by specifying a 0
    
- List of vertices:
    - each vertex represented by a 3 value tuple
    - specifies the X, Y, and Z co-ordinates of each vertex
    
- List of faces:
    - each face represented by a multi-value tuple
    - the first value of the tuple indicates the #vertices forming the face
    - the first value is followed by the indices of the composing vertices
    - the vertex indices are in order (indexed from 0)
    - optionally, RGB values for the face color can follow the elements of the faces


### Sample OFF File:

```
# avoid comments and spaces between lines/sections
# the comments and spaces are added for readability

# Line 1
OFF

# Line 2
# #vertices, #faces, #edges
8 6 12

# List of vertices
# X, Y, Z coordinates
 1.0  0.0 1.4142
 0.0  1.0 1.4142
-1.0  0.0 1.4142
 0.0 -1.0 1.4142
 1.0  0.0 0.0
 0.0  1.0 0.0
-1.0  0.0 0.0
 0.0 -1.0 0.0

# List of faces
# #vertices, vertices indexes, rgb values
4  0 1 2 3  255 0 0
4  7 4 0 3  0 255 0
4  4 5 1 0  0 0 255
4  5 6 2 1  0 255 0 
4  3 2 6 7  0 0 255
4  6 5 4 7  255 0 0
```