{
  "date" : "2023-01-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "OSC - OpenStreetMap Change File Format",
  "description":"Learn about OSC file format and APIs that can create and open OSC files.",
  "linktitle" : "OSC",
  "menu" : {
    "docs" : {
      "identifier":"gis-osc",
      "parent" : "gis"
    }
  },
  "lastmod" : "2023-01-02"
}

## What is an OSC file?

An OSC file is a Change File Format that is contains modified street map data for an existing .osm street map. It contains information about the changes to be incurred to the [OSM file](/gis/osm/). OSC file can have three possible types of modification operations on OSM data i.e. `insert`, `modify`, or `delete`. These change files are commonly used to export data out of OSM editor and import to another editor.

You can open OSC files with Merkaartar and osmchange software.

## OSC File Format

OSC files are commonly saved in JOSM file format where the changes are represented by tags. It starts with `osmChange` tag that indicates the beginning of the file. The sub-tags specify if it is an insert, modify or delete operation that is to be performed on the corresponding node in OSM file. The contents of a node actually contain the contents of an osm tag.

### OSC File Format Example

Following is an example of modify operation on a node. Each element must have a changeset ID and a version number.

```
<osmChange version="0.6" generator="acme osm editor">
    <modify>
        <node id="1234" changeset="42" version="2" lat="12.1234567" lon="-8.7654321">
            <tag k="amenity" v="school"/>
        </node>
    </modify>
</osmChange>
```

## References

* [JOSM File Format](https://wiki.openstreetmap.org/wiki/JOSM_file_format)
