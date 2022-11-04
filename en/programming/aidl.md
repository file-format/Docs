{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AIDL File - Android Interface Definition Language File",
  "description":"Learn about what is AIDL file format with example and APIs that can create and open AIDL files.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
    }
  },
  "lastmod" : "2022-10-30"
}

## What is an AIDL file?

An AIDL (Android Interface Definition Language) file allows Android developers to establish communication between different apps. Based on the programming interface, both the client and service agree to communicate using interprocess communicate (IPC). AIDL file contains [Java](/programming/java/) source code for defining these interfaces and contracts for communication between apps.

You can open AIDL files with Google Android Studio or any text editor such as Microsoft Notepad and Notepad++.

## AIDL File Format - More Information

AIDL are text files that contain the interfaces for communication between apps. Android OS doesn't allow one process to access the memory of another process. This leads the processes to split their objects into primitives for understanding of the underlying operating system and establish the process of communication structures for developer.

### What Data Types are supported by AIDL?

AIDL supports the following data types by default.

 * All primitive types in the Java programming language (such as int, long, char, boolean, and so on)
 * String
 * CharSequence
 * List
 * Map

## AIDL File Example

Following is an example AIDL file.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## References

 * [Android Interface Definition Language (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)
