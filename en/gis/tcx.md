{
  "date" : "2022-05-06",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "TCX File Format- Training Center XML File",
  "description":"Learn about TCX file format and APIs that can create and open TCX files.",
  "linktitle" : "TCX",
  "menu" : {
    "docs" : {
      "identifier":"gis-tcx",
      "parent" : "gis"
    }
  },
  "lastmod" : "2022-05-06"
}

## What is a TCX file?

A TCX (Training Center XML) file is a data exchange format used to share data between fitness devices. It was introduced in 2008 with Garmin's Training Center product. Workout data such as heart rate, running cadence, bicycle cadence, calories, and lap time is stored in [XML](/web/xml/) format inside the TCX file. In addition, summary data about the workout track is also included in the TCX file. TCX files are similar to [FIT](/gis/fit/) files that are created with Garmin sports wearable devices.

## TCX File Format - More information

TCX files are saved to disc as XML files with each record saved as an activity. An activity comprises all the data of a workout such as time, lap time, Id, heart-rate, intensity, cadence and track information that contains the pairs of position along with the timestamp for that lat-long position similar to the [GPX](/gis/gpx/) files.

### TCX File Format Versions

There are two versions of this format with their own XML schemas hosted by Garmin. Following are few of them:

 * https://www8.garmin.com/xmlschemas/TrainingCenterDatabasev2.xsd
 * https://www8.garmin.com/xmlschemas/UserProfileExtensionv1.xsd
 * https://www8.garmin.com/xmlschemas/ActivityExtensionv2.xsd


## TCX Data Protocol

A swift version of TCX XML format is available on Github as [TcxDataProtocol](https://github.com/FitnessKit/TcxDataProtocol).

## References ##

* [Training Center XML](https://en.wikipedia.org/wiki/Training_Center_XML)
* [TCX Viewer](http://www.whiterocksoftware.com/2019/02/tcx-viewer.html)
