{
  "date": "2023-09-27",
  "keywords": [
    "cfg",
    "cfg file",
    "cfg celestia configuration file",
    "what is a cfg file",
    "how to open cfg file",
    "file",
    "cfg file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "CFG File Format - Celestia Configuration File",
  "description": "Learn about CFG Celestia Configuration File format and APIs that can create and open CFG files.",
  "linktitle": "CFG Celestia",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-celestia",
      "parent": "settings"
    }
  },
  "lastmod": "2023-09-27"
}

## What is a CFG file?

A Celestia configuration file is plain text file used by Celestia, 3D universe simulation program. These files are vital for customizing how Celestia behaves, what celestial objects are displayed, and how program appears. However, editing these files requires careful attention because improper changes can disrupt Celestia's loading process, preventing it from running correctly.

## Celestia

Celestia is free, open-source 3D astronomy simulation software that allows users to explore and visualize universe in highly realistic and interactive manner. It was developed by Chris Laurel and was first released in early 2000s. Celestia is available for Windows, macOS, and Linux operating systems.

Key features and aspects of Celestia include:

- **Realistic 3D Visualization:** Celestia provides detailed and accurate representation of our solar system, as well as stars, galaxies, and other celestial objects. It uses high-quality 3D models and textures to create visually immersive experience.

- **Extensive Celestial Database:** The software comes with vast built-in database of known celestial objects, including stars, planets, moons, asteroids, comets, and spacecraft. Users can easily locate and explore these objects.

- **Scientific Accuracy:** While Celestia is visualization tool, it aims to represent celestial objects and phenomena as accurately as possible, based on available scientific data.

## File Formats Used by Celestia

Celestia utilizes various file formats for different aspects of its 3D astronomy simulation. Here are some of key file formats employed by Celestia:

1. **Configuration Files (.cel)**
   - *Description*: Plain text files that permit users to customize Celestia's behavior, appearance, and content.
   - *Purpose*: Customizing settings, defining locations, and specifying celestial objects.

2. **3D Models and Meshes**
   - *Formats*: [.3ds](/3d/3ds/), [.obj](/3d/obj/), [.dae](/3d/dae/), .ac
   - *Description*: Supported 3D model file formats used for rendering celestial bodies and spacecraft.
   - *Purpose*: Displaying 3D objects within Celestia.

3. **Texture Files**
   - *Formats*: [.jpg](/image/jpeg/), [.png](/image/png/), [.dds](/image/dds/)
   - *Description*: These files provide surface textures for celestial bodies.
   - *Purpose*: Mapping textures onto 3D models for realistic appearance.

4. **Star Catalogs and Data Files**
   - *Formats*: Custom formats, [.csv](/spreadsheet/csv/), [.tsv](/spreadsheet/tsv/)
   - *Description*: Data files used to represent stars and other celestial objects, ensuring accurate simulation.
   - *Purpose*: Accurate representation of celestial objects.

5. **Texture Cube Maps**
   - *Description*: Cube maps are used to simulate appearance of distant celestial objects like galaxies.
   - *Purpose*: Rendering distant objects with realistic textures.

6. **Script Files**
   - *Description*: These files contain custom scripts written in Celestia's scripting language.
   - *Purpose*: Enabling users to create dynamic events and animations within Celestia's universe.

## Celestia configuration file

Here is basic overview of what you can do with Celestia configuration file:

1. **Setting Your Location**: You can specify your location on Earth using latitude, longitude, and altitude parameters. This allows Celestia to accurately display night sky from your position.

```
Location "My Location"
{
    Latitude 40.7128
    Longitude -74.0060
    Altitude 0
}
```

2. **Customizing Your Viewing Options:** You can adjust various viewing options such as field of view, time settings, and rendering preferences.

```
Viewpoint
{
    Location "My Location"
    Follow "Earth"
    Eye [0.0 0.0 0.0]
    Center [0.0 0.0 0.0]
    Up [0.0 1.0 0.0]
    Fov 45
}

Time
{
    Date "2023-09-25T12:00:00.000Z"
    Clock "Now"
}

Rendering
{
    Atmosphere false
    Stars 7
    Planetshine 0.25
}

```

3. **Loading Celestial Objects:** You can add celestial objects such as stars, planets, asteroids, spacecraft, and more to your simulation. Each object is defined in configuration file with its properties.

```
Star "Sun"
{
    RA 0
    Dec 0
    Distance 0
    AppMag -26.74
    SpectralType "G2V"
}

Planet "Earth"
{
    Parent "Sol"
    Texture "earth.jpg"
    Radius 6371
    EllipticalOrbit
    {
        Period 365.25
        SemiMajorAxis 149.6e6
        Eccentricity 0.017
        Inclination 0
        AscendingNode 0
        ArgOfPericenter 102.94
        MeanAnomaly 100.464
    }
}
```

4. **Defining Spaceships:** You can create your own fictional spacecraft or use real ones by specifying their parameters like position, orientation, and 3D models.

```
Spacecraft "Voyager 1"
{
    Parent "Sol"
    Class "spacecraft"
    Mesh "voyager.3ds"
    Radius 0.01
    EllipticalOrbit
    {
        Period 30700
        SemiMajorAxis 1.08e11
        Eccentricity 0.044
        Inclination 3.4
        AscendingNode 49.0
        ArgOfPericenter 44.0
        MeanAnomaly 35.0
    }
}
```

5. **Creating Scripts:** You can write scripts in Celestia's custom scripting language to create dynamic events and animations.

## How to open CFG file?

Programs that open or reference CFG files

- Celestia (Free) for (Windows, Mac, Linux)

## Other CFG files

Here are other file types that use the **.cfg** file extension.

**Settings**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Game**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**System & Misc**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## References
* [Celestia](https://en.wikipedia.org/wiki/Celestia)
