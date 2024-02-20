{
  "date": "2022-05-06",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "FIT File Format- Garmin Activity File",
  "description": "Learn about FIT file format and APIs that can create and open FIT files.",
  "linktitle": "FIT",
  "menu": {
    "docs": {
      "parent": "gis",
      "identifier": "gis-fit"
    }
  },
  "lastmod": "2022-05-06"
}

## What is a FIT file?

An FIT file is a GIS file created by Garmin sports wearable devices. It is used to record the activities of the person when he/she moves wearing these devices. The activity data includes location and time as recorded by the GPS device. FIT files are also used to transfer the recorded activity data using web APIs. That is the reason FIT files are the most commonly used file format for sharing fitness data with other fitness platforms. Other common file formats include [GPX](/gis/gpx/), TCX, and [KML](/gis/kml/).

## FIT File Format - More Information

FIT files are saved to disc as binary files with the information recorded by the Garmin devices for the activity. Information stored inside a FIT file includes:

 * Date & time
 * Sport types
 * Lap & split data
 * GPS track
 * Sensor data
 * Events for active session

Activity data can be recorded in the file in real time or exported once the activity recording is complete.

### FIT Activity Messages

A FIT activity file may include some required message types. The following are the required messages for an activity file.

|Message|Purpose|
---|---|
|File Id| The File Id message is required by all FIT file types and is expected to be the first message in the file. For Activity files, the Type property should be set to 4.|
|Activity| A single Activity message is required in a FIT Activity file. Included in the Activity message are the Local Timestamp and Session Count properties. The Local Timestamp is used to determine the time zone offset that can be applied to all timestamps in the file. Most devices record FIT files in real time and the session count will be unknown until the end of the recording. Because of this, the Activity message will often be the last message in the file.|
|Session| Activity files will contain one or more Session messages. A Session message is a Summary message type. Start Time, Total Elapsed Time, Total Timer Time, and Timestamp are required fields for all summary messages.|
|Lap| Lap messages represent laps or intervals within the session. A Lap message is a Summary message type. Start Time, Total Elapsed Time, Total Timer Time, and Timestamp are required fields for all summary messages.|
|Record| Record messages include GPS coordinate, speed, distance, heart rate, power, etc.|

## FIT File Useful Resources

 * [Decoding FIT Activity Files](https://developer.garmin.com/fit/cookbook/decoding-activity-files/)
 * [Encoding FIT Activity Files](https://developer.garmin.com/fit/cookbook/encoding-activity-files/)
 
## References ##

* [FIT Activity File](https://developer.garmin.com/fit/file-types/activity/)
