{
  "date": "2023-08-03",
  "keywords": [
    "usr",
    "usr file",
    "what is a usr file",
    "how to open usr file",
    "file",
    "usr file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "USR File Format - Lowrance GPS Data File",
  "description": "Learn about USR format and APIs that can create and open USR files.",
  "linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr",
      "parent": "gis"
    }
  },
  "lastmod": "2023-08-03"
}

## What is a USR file?

The ".usr" file extension is also related to Lowrance GPS devices. In particular, it is used for storing GPS data in a format known as "User Data Format" (USR format) which is used by Lowrance GPS devices.

When using a Lowrance GPS unit, you can save your waypoints, tracks, and routes as ".usr" files. These files typically contain information such as latitude, longitude, altitude, timestamp, and other data related to your GPS activities.

Here are some common uses of .usr files with Lowrance GPS devices:

- **Waypoints:** Waypoints are specific locations marked on the GPS, such as landmarks, favorite fishing spots, or points of interest. You can save these locations as .usr files, and they can be imported, exported, or shared with other Lowrance GPS users.

- **Tracks:** Tracks represent the recorded path of your GPS movements. You can save your track logs as .usr files, allowing you to review and analyze your routes later or share them with others.

- **Routes:** Routes are pre-defined paths that you can create and save on your GPS device. These routes can also be saved as .usr files for future use or sharing.

To manage .usr files on your Lowrance GPS device, you typically use software like Lowrance's "Insight Planner" or "Lowrance GPS Utility" to import, export, and manipulate your GPS data.

## USR File Format - More Information

In Lowrance iFinder GPS devices, the .usr files are created and saved on the MultiMediaCard (MMC) memory card inserted into the device. These files contain user data such as waypoints, tracks, and routes.

To transfer the .usr files from the MMC to a computer, you can follow these steps:

- **Remove the MMC:** Carefully remove the MultiMediaCard (MMC) from the Lowrance iFinder GPS device.

- **Insert MMC into Computer:** Use an appropriate MMC card reader to insert the memory card into your computer's card reader slot.

- **Locate .usr Files:** Once the MMC is recognized by your computer, you should be able to access the files stored on it. Look for the .usr files, which contain your GPS data.

- **Conversion with GPSBabel:** To convert the .usr files to another GPS format, you can use GPSBabel, which is a free and open-source tool for working with various GPS file formats. GPSBabel supports a wide range of input and output formats, allowing you to convert the .usr files to formats compatible with other GPS software or devices.

You can download GPSBabel from the official website (http://www.gpsbabel.org/) and install it on your computer. Once installed, you can use the software's command-line interface or graphical user interface (if available) to perform the conversion.

For example, if you want to convert .usr files to GPX format, you can use a command like:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

The above command instructs GPSBabel to read the input file "input.usr" in Lowrance USR format and write the output file "output.gpx" in GPX format.

- **Importing/Using Converted Files:** After the conversion, you'll have your GPS data in the new format (e.g., GPX), which you can use with other GPS software or devices that support that format.

## How to open USR file?

Programs that open or reference USR files include

- GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## References
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)
