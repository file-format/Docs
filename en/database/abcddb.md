{
  "date" : "2023-01-09",
  "keywords" : [ "ABCDDB", "what is a ABCDDB file", "extension", "file", "file format", "Database File Type", "Database File Format", "Database Files" ],
  "author" : {
    "display_name" : "Shakeel Faiz"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about ABCDDB file format and APIs that can create and open ACCDB files.",
  "title" : "ABCDDB File Format - Apple Address Book Contact List Database File",
  "linktitle" : "ACCDB",
  "menu" : {
    "docs" : {
      "identifier":"database-abcddb",
      "parent" : "database"
    }
  },
  "lastmod" : "2020-01-09"
}

## What is an ABCDDB file?

The file with extension **.ABCDDB** stands for Apple Address Book Contact List Database. It belongs to **Address Book** application also commonly known as **Contacts**. It is a built-in application and included with iOS and macOS operating systems. Contacts application enables users to save and organize information related to their contacts, including individuals, businesses, and organizations. This app allows users to keep track of details such as names, addresses, phone numbers, and email addresses, as well as to categorize their contacts into groups. 

## Relation with SQLite and Typical Path

Apple's AddressBook (also known as Contacts) stores contact information as vCards in the metadata folder. **The file _ABCDDB_ is actually _SQLite 3 datafile_**. 

SQLite is a popular database management system that is designed to be lightweight and self-contained. It is used in many different types of software and devices. SQLite is a type of RDBMS, meaning it stores data in tables that are related to one another through keys. It can handle a range of data types, including integers, floating-point numbers, strings, and binary data. Additionally, SQLite supports transactions, which enable users to perform multiple database operations together as a single unit of work.

The file with ABCDDB extension is typically stored here

`~/Library/Application Support/AddressBook/AddressBook-v22.abcddb`

## Fixing up corrupt Contacts database

Please first take the backup before attempting to do this. Then please navigate to 

`~/Library/Application Support/AddressBook`

In that directory, you will find three files including the one with .abcddb extension

- `addressbook-v22.abcddb`
- `addressbook-v22.abcddb-wal`
- `addressbook-v22.abcddb-shm`

Delete all these files and reopen the Contacts it will start working again.

## Restore AddressBook database from Backup

Assume, your AddressBook database contacts are stored in `addressbook-v22.abcddb`

- First backup your AddressBook data and quit all applications.
- Move your database file to `~/Library/Application Support/AddressBook` subdirectory
- Launch **Address Book.app**.

## Export ABCDDB file data to Microsoft Access

Since the file is SQLite 3 datafile, you can export the data inside abcddb file into Microsoft Access using ODBC connector.

The SQLite ODBC connector is a software library and driver that enables applications that support the ODBC interface to connect to a SQLite database. It includes a library that defines the ODBC interface, and a driver that translates this interface into calls to the SQLite API. To utilize the SQLite ODBC connector, you must first install it and then set up an ODBC data source on your computer. After completing these steps, any application that is equipped with ODBC support will be able to connect to the data source and retrieve data from the SQLite database.

## References
 * [Fix corrupted Contacts database](https://discussions.apple.com/docs/DOC-10581)
 * [Contact Database For Mac](https://nitroreward.weebly.com/blog/contact-database-for-mac)
 * [How can I open or export a abcddb file in Windows 7 Excel?](https://apple.stackexchange.com/questions/52888/how-can-i-open-or-export-a-abcddb-file-in-windows-7-excel)
