{
  "date" : "2021-06-14",
  "keywords" : [ "LOG", "extension", "log file", "log file format", "Database File Type", "Database File Format", "what is a log file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about LOG file format and APIs that can create and open LOG files.",
  "title" : "LOG - Log File Format",
  "linktitle" : "LOG",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-06-14"
}

## What is a LOG file?
A file with .log extension contains the list of plain text with timestamp. Usually, certain activity detail is logged by the softwares or operating systems to help the developers or users to track what was happening at a certain time period. Users can edit these files very easily by using any text editors. Usually the error reports or login activities are logged by the operating systems, but other softwares or web servers also generate log files to track visitors and to monitor bandwidth usage.

## LOG File Format
The LOG file format records the typical events that occur either in an operating system, messages between different users of a communication software or any other software runs. Simply we can say that certain messages at certain time stamps are logged in a LOG file. Some commonly used terms for logging are:
### Event Logs
It Records events occur in the execution of a system in order to track and understand the activity of the system and to diagnose problems. They are important to identify the activities of complex systems, typically in the case of applications with very little user interaction.
### Transaction logs
Almost all database systems maintain the transaction log, which are not usually intended as an audit trail for later analysis, and are not human-readable. These logs only keep the record of changes to the existing data to enable the database to recover from crashes or other data errors and keep the data in a consistent state. Hence, database systems usually have both general event logs and transactional logs.
### Message logs
The textual communication saved by Internet Relay Chat (IRC), instant messaging (IM) programs, peer-to-peer file sharing clients with chat functions, and multiplayer games (especially MMORPGs)are called message logs. These logs are generally saved in plain text files, but IM and VoIP clients (e.g. Skype) might save them in HTML files to ease reading or enable encryption.
### Server logs
Server log is actually a log file containing the a list of activities that performed and created or maintained automatically by the server itself.  Usually these files are not accessible to general Internet users, only to the webmaster or other administrative person of an Internet service.



## References ##

* [Log file - Wikipedia](https://en.wikipedia.org/wiki/Log_file)
