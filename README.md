# morpho-vtk

Morpho package for reading and writing meshes and fields in the legacy VTK unstructured-grid format.

The module depends on the core `meshtools` and `parser` modules.

## Installation

You can install the package with morphopm in the Terminal app:

    morphopm install vtk

Load it in Morpho with:

    import vtk

Help is available from the Morpho prompt with `? vtk`.

## Usage

The VTK package can be used to export and import `Mesh`s, and `Field`s.

    import vtk
    import meshtools

    var m = LineMesh(fn (t) [t, 0, 0], -1..1:2)
    var vtkE = VTKExporter(m)
    vtkE.export("mesh.vtk")

    var vtkI = VTKImporter("mesh.vtk")
    print vtkI.mesh()

`VTKExporter` accepts a `Mesh` or a `Field`. `addField` attaches further vertex fields. `VTKImporter` returns the mesh and looks up fields by the name stored in the file.

Fields must live on vertices (shape `[1,0,0]`) and be a scalar or a 2D/3D column vector.

## Tests

From the `test` directory:

    python test.py

The repository root must appear in `~/.morphopackages` so `import vtk` loads this package rather than a bundled copy.
