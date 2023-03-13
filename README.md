# 3D Object Classification

## OFF File:
---

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