{
  "date" : "2021-07-29",
  "keywords" : [ "md5 file", "md5 file format", "what is an md5 file", "file", "md5 example", "md5 file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MD5 - MD5 Checksum File",
  "description":"Learn about MD5 file and APIs that can create and open MD5 files.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
    }
  },
  "lastmod" : "2021-07-29"
}

## What is an MD5 file?

An MD5 file is a checksum file used for the verification of a file's integrity. It is similar to a fingerprint for the associated file and is uniquely generated using an algorithm that uses the number of bits in the file. It is used to verify the file with software such as [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). One advantage of using MD5 files is to verify that the downloaded files are not corrupt.

## MD5 File Format - More Information

Usually an MD5 file is saved with the same name as the original file name but with the .md5 extension. For example, if the associated file name is `abc_987_123456.grb`, the corresponding MD5 file name will be `abc_987_123456.grb.md5`. MD5 files help identify that a received or downloaded file is not corrupted or affected by malicious content. In short, MD5 files guarantee the completeness of a file.


## How to check MD5 Checksum?

A single file can be checked/verified for MD5 using the [md5sum](https://en.wikipedia.org/wiki/Md5sum) tool as follow.

```
md5sum -c abc_987_123456.grb.md5
```

## References

* [md5sum - Wikipedia](https://en.wikipedia.org/wiki/Md5sum)
