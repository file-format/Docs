{
  "date": "2020-03-02",
  "keywords": [
    "SVG",
    "file",
    "file format",
    "Page Description Language",
    "Scalar"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about SVG file format and APIs that can create and open SVG files.",
  "title": "What is an SVG file?",
  "linktitle": "SVG",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-svg"
    }
  },
  "lastmod": "2020-03-02"
}

## What is an SVG file? ##

An SVG file is a Scalar Vector Graphics file that uses XML based text format for describing the appearance of an image. The word Scalable refers to the fact that the SVG can be scaled to different sizes without losing any quality. Text-based description of such files makes them independent of resolution. It is one of the most used formats for building a website and print graphics in order to achieve scalability. The format can only be used for two-dimensional graphics though. SVG files can be viewed/opened in almost all modern browsers including Chrome, Internet Explorer, Firefox, and Safari.

## Brief History ##

SVG specifications are available as open standard by World Wide Web Consortium (W3C) since 1999. Before this, similar file format specifications in six different formats were submitted to W3C till 1998. An update was applied to the specifications in 2011 and it was versioned 1.1. In 2016, SVG 2 was published as newer version including features in addition to those in SVG 1.1.

## File Format Specifications ##

The SVG Document Object Model (DOM) lays the foundations for all the specifications and interfaces that correspond to the particular sections of the specifications. SVG viewers must implement the SVG DOM interfaces as defined throughout the W3C specifications. Its DOM exposes several interfaces for different data types and elements.

### SVG shapes ###

SVG has some predefined shape elements that can be used by developers:

* Rectangle <rect>
* Circle <circle>
* Ellipse <ellipse>
* Line <line>
* Polyline <polyline>
* Polygon <polygon>
* Path <path>

Based on these shapes and specifications, functional areas of SVG are as follow.

**Paths** - Paths are used to represent simple as well as compound shape outlines. Codings are used to define the nature of operation. For example, M is used for Move To, L is used for Line To, Z is used to close a path and so on.

**Basic Shapes** - Straight-line paths and paths made up of a series of connected straight-line segments (polylines), as well as closed polygons, circles, and ellipses can be drawn. Rectangles and round-cornered rectangles are also standard elements.

**Text** - Text representation is expressed as XML character data where many visual effects can be applied to the text. The specifications allow to handle bidirectional text, vertical text and characters along a curved path.

**Painting** - Shapes can be filled and/or outlined with a colour, a gradient or a pattern, allowing the capability to make it opaque or have any degree of transparency. Line-end features such as arrowheads or symbols appearing at the vertices of a polygon are represented by Markers.

**Color** - SVG specifications allow to apply colours to all visible SVG elements, either directly or via fill, stroke, and other properties. Different colour codings can be used for specifying like black or blue, hex representation, decimal or as percentages of the form RGB.

**Gradients and Patterns** - Shapes in an SVG file can be filled or outlined with solid colours, gradients or repeating patterns.

**Filter Effects** - Its actually a series of graphics operations that are applied to given source vector graphic to produce modified result.

**Interactivity** - Users can interact with SVG files by changing focus, mouse clicks, scrolling or zooming the image. The Interactivity lets SVG images interact with users in many different ways as aforementioned.

**Linking** - It is possible for SVG images to have hyperlinks to other documents. This is achieved via the XML Linking Language or XLink. This allows for creating specific view states that are used to zoom in/out of a specific area or to limit the view to a specific element.

**Scripting** - Similar to HTML, all aspects of an SVG document are accessible for manipulation using scripts. The SVG DOM objects provides the guidance for achieving this using SVG element and attribute. Scripts are enclosed in `script` tag elements and can run in response to pointer, keyboard or document events as required.

**Animation** - The DOM elements <animate>, <animateMotion> and <animateColor> lets you to including animation for SVG contents. Of course, this is not achievable without using scripts and built-in timers. These animations can be continuous and can be put on loop as well as repeats while at the same time responding to user events.

**Fonts** - Text in SVG can reference external font files such as system fonts. In absence of such fonts, text in SVG will not be rendered to the output. This can be overcome by incorporating the required glyphs in such a file as a font that is then rendered using the <text> element.

## Examples ##
The following lines show how a Circle is represented using the SVG script.

```
<html>
<body>

<h1>My first SVG</h1>

<svg width#"100" height#"100">
  <circle cx#"50" cy#"50" r#"40" stroke#"green" stroke-width#"4" fill#"yellow" />
</svg>

</body>
</html>
```

 The following lines of code show how to use the <text> block for rendering text to SVG.

```
<svg height#"30" width#"200">
  <text x#"0" y#"15" fill#"red">I love SVG!</text>
</svg>
```

## References ##

* [W3C SVG Specifications](https://www.w3.org/TR/SVG2/Overview.html)
* [SVG - Wikipedia](https://en.wikipedia.org/wiki/Scalable_Vector_Graphics)
