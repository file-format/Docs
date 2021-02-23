{
  "date" : "2021-02-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MJPEG - Motion JPEG File Format",
  "description":"Learn about MJPEG file format and APIs that can create and open MJPEG files.",
  "linktitle" : "MJPEG",
  "menu" : {
    "docs" : {
      "parent" : "video"
    }
  },
  "lastmod" : "2021-02-16"
}

## What is a MJPEG file?

A file with .mjpeg (Motion JPEG) extension is a video file that is created by compressing individual video frame as a JPEG image. It is different from the standard MPEG-1 and MPEG-2 file formats where the compression is interframes and is decided based on the prediction of contents in subsequent frames. MJPEG is supported by wide range of applications that include web browsers, media players, digital cameras, webcams, streaming servers. Plug-ins are available for applications that want to make use of the MJPEG file format.

## MJPEG File Format

MJPEG is based on the mature cmopression standard i.e. [JPEG](/image/jpeg/) that has well-defined libraries. It could not be standardized similar to standards such as MPEG-2 and there is no documentation available that can be referred to as complete specifications for the "Motion JPEG". In the absence of such a standard, outputs from different manufacturers can raise compatibility issues. However, companies like Microsoft and Apple has documented how the M-JPEG files are stored in their native formats such as [AVI](/video/avi/) and [QT](/video/qt/). The [rfc2435](https://tools.ietf.org/html/rfc2435) describes the RTP Payload Format for JPEG-compressed Video and can be consulted as reference material.

## References

- [RFC2435 - RTP Payload Format for JPEG-Compressed Video](https://tools.ietf.org/html/rfc2435)
- [Motion JPEG - Wikipedia](https://en.wikipedia.org/wiki/Motion_JPEG)
