Changelog for the Metabolize fork
=================================

## 1.2.1 (Oct 5, 2018)

- Use the new `vector_shortcuts` package.


## 1.2.0 (Oct 4, 2018)

As of this release, break from the upstream revision history and adopt ordinary
semver.

Features:

- Add `has_same_topology()` helper.
- Add `face_indices_to_flip` parameter to `flip_faces()`
- `quads_to_tris` optionally returns a mapping of old quads to new tris.
- Add new method `reorient_faces_using_normals()`

Improvements:

- Replace for loops in `flip_faces()` with vectorized operations
- Re-enable test for `flip_faces()`.
- Delegate shape geometry generation to `blmath`. Requires `1.2.5.post3` or
  later.
- `landm` / `barycentric`: Refactor + improve readability

Note: This release does not include quad face support from `1.1.8.dev1`.


## 1.1.8.dev1 (Sep 9, 2018)

- Increased support for quad faces
    1. Reading a quad mesh's faces, normals, and texture coordinates from an OBJ. f4, fn4, and ft4 are set in addition to f, fn, and ft which hold the triangulated faces as before.
    2. Writing a mesh with quad faces to OBJ. `write_obj` prioritizes f4, fn4, and ft4 over the triangulated faces.
    3. `keep_vertices` operates correctly on either f and f4, though you need to `del` the one you don't want updated.

This is an experimental release, with API and behavior subject to change in
future `.post` releases. Refer to the API in
[#9](https://github.com/metabolize/lace/pull/9). Track the development in
[#2](https://github.com/metabolize/lace/pull/2).


## 1.1.8.post1 (Sep 9, 2018)

Substantively identical to upstream 1.1.8.