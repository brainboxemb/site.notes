# OpenSCAD

OpenSCAD is a script-based CAD application for creating parametric 3D models.

Instead of drawing a model directly, the geometry is described using code. This makes it useful for designs where dimensions, repetitions and variants need to be adjusted later.

- [OpenSCAD](https://openscad.org/)
- [OpenSCAD Documentation](https://openscad.org/documentation.html)

## Possible Uses

OpenSCAD can be useful for:

- Designing brackets and mounting parts
- Creating parametric enclosures
- Modelling repeated patterns
- Generating multiple size variants
- Preparing models for 3D printing
- Documenting dimensions directly in source code

## Examples and Tutorials

- [OpenSCAD example by Keith Neufeld](http://www.neufeld.newton.ks.us/electronics/?p=1730)  
  An OpenSCAD example showing how a model can be created and adjusted using source code.

- [Managing OpenSCAD Projects](https://www.maskset.net/blog/2025/05/16/managing-openscad-projects/)  
  An article about structuring larger OpenSCAD projects using reusable modules, libraries, `OPENSCADPATH`, Makefiles and separate files for assemblies and exported parts.

## Example

```openscad
width = 40;
depth = 30;
height = 10;

cube([width, depth, height]);