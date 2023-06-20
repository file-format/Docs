{
  "date" : "2021-01-22",
  "keywords" : [ "ASE","file", "format", "file type", "extension","what is an ASE file?" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about ASE file format and APIs that can open and create ASE files.",
  "title" : "ASE - Autodesk ASCII Scene Export File",
  "linktitle" : "ASE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2021-01-22"
}

## What is an ASE file?

A file with a .ase extension is an Autodesk ASCII Scene Export file format that is an ASCII representation of a scene, containing 2D or 3D information while exporting scene data using Autodesk. Autodesk provides options to include scene components while exporting scene data. You can include Mesh definition along with vertex and face information, Material description, transform animation data for the objects, complete mesh definition of every n frames, animation data for cameras and lights and IK joint settings.

## ASE File Format - More Information

ASE files are text files stored in ASCII format that can be opened in any text editor. An ASE file can contain the following types of information provided by Autodesk.

### Output Options

 * `Mesh Definition` - Exports the definition of each mesh, including vertex and face information for geometric objects. In addition, turning this on enables the items in the Mesh Options group box, described below.
 * `Materials` - Includes the material description. If a material is not assigned to an object, its wireframe color is exported. All levels of a material tree are included, so this can produce a lot of text.
 * `Transform Animation Keys` - Includes the transform animation data for the objects. If the object is a target camera or spotlight, this will include target animation data.
 * `Animated Mesh` - Exports a complete mesh definition of every n frames. The frequency is specified by the Controller Output spinner, described below. Each block contains the same information specified in the Mesh Options group box, described below. Turning this on can result in a huge file, even for small scenes.
 * `Animated Camera/Light Settings` - Exports the animation data for cameras and lights, such as color, intensity, falloff, map bias, and so on. Outputs a block every n frames, as specified by the Controller Output spinner.
 * `Inverse Kinematic Joints` - Exports the IK joint settings in the Hierarchy branch.

### Object Types

The items here let you specify which category of object you want included in the output. You can include geometric objects, shapes, cameras, lights, and helper objects.

 * Geometric
 * Shapes
 * Cameras
 * Lights
 * Helpers

### Mesh Options

 * `Mesh Normals` - Exports the face and vertex normals. The normal of the face is listed first, followed by the normals of the three vertices supporting the face. Turning this on results in a much larger file.
 * `Mapping Coordinates` - Exports a list of mapping vertices and faces, according to the TVert and TVFace structures described in the 3ds Max Software Development Kit. If an object uses face mapping, a face map list is exported containing UVW coordinates for each face.
 * `Vertex Colors` - Exports vertex colors.

### Controller Output

 * `Use Keys` - Exports key values. If the controller doesn't use keys, then the Force Sample method is used. In the case of transform controllers, the Use Keys option works only if all of the transform controllers are either Linear/TCB or Bezier. If one of the transform tracks uses a different type of controller, then the Force Sample method is used for all transform tracks.
 * `Force Samples` - Samples controller values based on the frequency specified in the Frames per Sample Controller.

## References

 * [Autodesk - Exporting to ASCII](https://help.autodesk.com/view/3DSMAX/2020/ENU/?guid=GUID-98B2388D-A3A7-4096-8E81-888A3F9D6069)
