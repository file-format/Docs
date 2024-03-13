{
  "date": "2022-06-06",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TPSR File Format - TeamViewer Pilot Session Report File",
  "description": "Learn about TPSR file format and APIs that can create and open TPSR files.",
  "linktitle": "TPSR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tps-azr"
}
},
  "lastmod": "2022-06-06"
}

## What is a TPSR file?

A TPSR is a connection protocol file used by the TeamViewer Assist AR (previously known as TeamViewer Pilot). Information stored in a TPSR file is stored in compressed [ZIP](/compression/zip/) file format. TPSR contains detailed history of TeamViewer connection between an expert and a technician for resolving  issue and reviewal purpose. Information contained inside a TPSR file includes device type, name, Assist AR ID, Expert ID, date and time, and duration of the connection. This data is stored in a [JSON](/web/json/) file inside the compressed TPSR archive.

## TPSR File Format

A TPSR file is stored to disc in ZIP archive file format where the contents are stored inside a JSON file. It is automatically generated after the completion of the Assist AR connection provided the Connetion reporting option is enabled in TeamViewer.

TeamViewer Assist AR lets experts connect to technicians to get LIVE feed of remote end via the mobile camera. They can assist the technicians for resolving the issue over the phone.

## Open TPSR Files

You can open TPSR files using the desktop version of TeamViewer software. If installed on your compture, double-clciking the TPSR file will open it in TeamViewer software. TPSR files can be exported to [PDF](/pdf/) files as well or can be printed to have a printed copy of the protocol file.

## References ##

* [TPSR](https://community.teamviewer.com/English/kb/articles/46456-using-teamviewer-assist-ar)


