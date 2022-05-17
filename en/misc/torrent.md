{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Torrent File Format - BitTorrent File",
  "description":"Learn about TORRENT files and APIs that can create and open TORRENT files.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
    }
  },
  "lastmod" : "2022-01-12"
}

## What is an TORRENT file?

A TORRENT file is a text file that is used by BitTorrent and other P2P (peer-to-peer) programs for download and exchange of content. The downloadable content may include documents, videos, games, movies, and other media available on the internet. It includes metadata information about the contents and location of the media to be downloaded. Software like BitTorrent uses information from this file such as name, file size, and folder structure for download of data. Torrent files can be converted to other file formats such as [PDF](/pdf/) online.

## What is Torrenting? The TORRENT File Format for Data Exchange

Torrenting is the concept of exchange (downloading and uploading) of data files using the BitTorrent network. Unlike conventional servers where data is uploaded for others to access and download, torrent files are retrieved and sent using the torrent network. When a user opens a .torrent file in applications such as BitTorrent, the software starts downloading the contents of the file bitwise. If multiple users have the same file, BitTorrent splits downloads among all the users to speed up the process of downloading. At the same time, the computer of the user who is downloading the file, also becomes the source of file for sending it to other users who are also downloading the same file.

### Structure of a TORRENT File

A torrent file is a combination of a list of files and metadata information about all the pieces of the file to be downloaded. It contains the following information in the form of keys.

 - `announce` — The URL of the tracker that is announced to other peers for informing about the availability of the file
 - `info` — This maps to a dictionary whose keys are dependent on whether one or more files are being shared:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
    - `length` — size of the file in bytes.
    - `path` — a list of strings corresponding to subdirectory names, the last of which is the actual file name
 - `length` — the size of the file in bytes (only when one file is being shared)
 - `name` — filename where the file is to be saved
 - `piece length` — number of bytes per piece. This is commonly 28 KiB = 256 KiB = 262,144 B.
 - `pieces` — a hash list that is a concatenation of each piece's SHA-1 hash.

## Is Torrenting Safe and Legal?

Torrenting protocol for exchange of data between P2P users is safe as it is just the means of sharing any type of file. Thus, the protocol itself is not unsafe or illegal. However, the content shared via the network may contain files or media that can violate the legal status of the shared documents. In such case, the exchange of such data can cause legal actions against the parties involved in sharing of such files publicly.

## References

* [TORRENT File - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)
