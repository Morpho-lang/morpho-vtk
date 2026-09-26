# Remove bundled vtk from Morpho-lang/morpho

Do this after morpho-vtk is the copy users import. Paths are relative to the morpho repository root.

CMake installs `modules/*.morpho` and `help/*.md` by glob, so deleting the files is enough. No `CMakeLists.txt` edit.

## Delete

- `modules/vtk.morpho`
- `help/vtk.md`
- `test/vtk/data.case2.vtk`
- `test/vtk/data.case3.0.vtk`
- `test/vtk/data.vtk`
- `test/vtk/ensurevtkfilename.morpho`
- `test/vtk/export_and_import_mesh.morpho`
- `test/vtk/export_and_import_no_fieldname.morpho`
- `test/vtk/export_and_import_scalar.morpho`
- `test/vtk/export_and_import_scalar_and_vector.morpho`
- `test/vtk/export_and_import_vector.morpho`
- `test/vtk/export_and_import_vector_2d.morpho`
- `test/vtk/export_import_2d.morpho`
- `test/vtk/export_import_3d.morpho`
- `test/vtk/export_incorrect_field_4d_vector.morpho`
- `test/vtk/export_incorrect_field_grade1.morpho`
- `test/vtk/export_incorrect_field_grade2.morpho`
- `test/vtk/export_incorrect_field_tensor.morpho`
- `test/vtk/import_external_vtk.morpho`
- `test/vtk/import_mesh.morpho`
- `test/vtk/import_scalar.morpho`
- `test/vtk/import_scalar_vector.morpho`
- `test/vtk/import_vector.morpho`
- `test/vtk/importer_containsfield.morpho`
- `test/vtk/importer_fieldlist.morpho`
- `test/vtk/importer_incorrect_fieldname.morpho`
- `test/vtk/mesh.vtk`
- `test/vtk/mesh_scalar.vtk`
- `test/vtk/mesh_scalar_vector.vtk`
- `test/vtk/mesh_vector.vtk`
- `test/vtk/rbc_001.vtk`
- `test/vtk/square.mesh`
- `test/vtk/square.vtk`
- `test/vtk/tetrahedron.mesh`
- `test/vtk/tetrahedron.vtk`
- `test/vtk/vtk_exporter_addfield_fname_not_str_err.morpho`
- `test/vtk/vtk_exporter_fname_not_str_err.morpho`
- `test/vtk/vtk_exporter_init_err.morpho`
- `test/vtk/vtk_exporter_invalid_fname_err.morpho`

## Edit

- `help/index.rst` — remove the `vtk` entry from the Modules toctree.

## Leave

- `releasenotes/version-0.5.2.md` records that vtk shipped in 0.5.2. Keep it.
