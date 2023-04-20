{
  "date": "2023-04-20",
  "keywords": [
    "ldb file",
    "what is an ldb file",
    "what information ldb contains",
    "what is the purpose of ldb file",
    "ldb extension",
    "file",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "LDB File Format - Microsoft Access Lock File",
  "description": "Learn about LDB format and what information does it contain.",
  "linktitle": "LDB",
  "menu": {
    "docs": {
      "identifier": "misc-ldb",
      "parent": "misc"
    }
  },
  "lastmod": "2023-04-20"
}

## What is an LDB file?

An LDB file is a lock file used by Microsoft Access to prevent multiple users from editing same database simultaneously. When user opens an Access database, Access creates a corresponding LDB file in same directory as the database. This file contains information about who is currently using database and what records they are editing.

The LDB file is automatically created by Microsoft Access when database is opened, and is deleted when database is closed. It is important to note that the LDB file should never be deleted manually because this can cause problems with the database.

If you encounter issues with Microsoft Access database, one potential solution is to try deleting LDB file associated with that database. This will release any locks that may be preventing you from accessing the database. However, be sure to make a backup of database before attempting this, as deleting the LDB file can cause data loss or corruption if done improperly.

## LDB File Format - More Information

An LDB file in Microsoft Access contains information about users who are currently accessing the database such as their user name, computer name and login time. The LDB file also contains information about any locks that have been placed on database, such as which records are being edited by which user.

Here is more detailed list of the types of information that can be found in an LDB file:

- **User name** - the name of the user who is currently accessing database
- **Computer name** - the name of the computer where the user is accessing database from
- **Login time** - the time when the user first opened the database
- **Record locks** - information about which records are currently being edited by which user
- **Object locks** - information about which database objects (such as tables, forms or reports) are currently being edited by which user
- **Connection information** - information about how user is connected to database (for example, whether they are using local or network connection)

The information in the LDB file is used by Microsoft Access to prevent multiple users from making conflicting changes to same database at same time. When user attempts to edit a record or object that is already locked by another user, Microsoft Access will display a message indicating that the object is already in use. The LDB file is updated as users open and close database and make changes to locked objects.

## References
* [What is an LDB File?](https://learn.microsoft.com/en-us/office/troubleshoot/access/ldb-file-description)
