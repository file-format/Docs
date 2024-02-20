{
  "date": "2020-07-28",
  "keywords": [
    "HPGL",
    "File Format",
    "Open",
    "Read",
    "Create",
    "CAD"
  ],
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about HPGL file format and APIs that can create and open HPGL files.",
  "title": "HPGL File Format - Learn from File Format Experts!",
  "linktitle": "HPGL",
  "menu": {
    "docs": {
      "parent": "cad",
      "identifier": "cad-hpgl"
    }
  },
  "lastmod": "2020-07-28"
}

## What is a HPGL file?

An HPGFL(Hewlett-Packard Graphics Language) file contains instruction set for plotter control by developed by HP. HP plotters use this file to draw and print vector and raster content on the paper.

### HPGL Command

An HPGL command consists of the following.
 * A command section of the alphabet of two characters
 * A parameter section
 * Terminator section

Each parameter in the file has to be devided with a separator in case of multiple parameters.

### HPGL Command Example

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Coordinate System

Coordinates systems comprises of 2-dimensional measurement indicators to locate any specific location. The HPGL uses both Plotter coordinate and user coordinate system for this purpose.

#### Plotter Coordinate System

This coordindate system is used to plot drawings based on plotter movement. A typical XY unit of minimum plotter movement is 0.025mm. The possible range of drawing changes with plotter kinds.

#### User coordinate system

User specified coordinate system can be set up using the scale and origin. These are converted to plotter coordinates using the IP command and SC command. Plotter system coordinates are used by default if this conversion is not carried out.

## HPGL File Format
HPGL files are in ASCII (text file) format and start with few setup commands. This sets up certain parameters for the plotter for plotting. A typical HPGL file looks as follow.

|Command|Meaning
---|---|
|IN;|initialize, start a plotting job|
|IP;|set the scaling points (P1 and P2) to their default positions|
|SP1;|select pen 1|
|PU0,0;|lift Pen Up and move to starting point for next action|
|PD100,0,100,100,0,100,0,0;|put Pen Down and move to the following locations (draw a box around the page)|
|PU50,50;|Pen Up and move to X,Y coordinates 50,50|
|CI25;|draw a circle with radius 25|
|SS;|select the standard character set|
|DT*,1;|set the text delimiter to the asterisk, and do not print them (the 1, meaning "true")|
|PU20,80;|lift the pen and move to 20,80|
|LBHello World*;|draw a label|

## References
 * [HPGL by Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
 * [HPGL Reference Guide](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)
