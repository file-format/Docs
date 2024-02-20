{
  "date": "2023-05-17",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "description": "Learn about NMONEY file format and APIs that can create and open NMONEY files.",
  "title": "NMONEY File - Denaro Account File Format",
  "linktitle": "NMONEY",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-nmoney"
    }
  },
  "lastmod": "2023-05-17"
}

## What is an NMONEY file?

An NMONEY file is a financial data storage database file that contains track record of financial transactions. It was developed by Nickvision and was used int he Nickvision Denaro software which is a personal financial software application. Data stored inside a NOMONEY file includes credit and debit transactions information to an account.

NOMONEY files can be opened with [Github](https://github.com/NickvisionApps/Denaro) application.

## About Denaro Software

Denaro was initially developed by [Nickvision](https://nickvision.org/) as a product that was later converted to an open-source software app hosted on [Github](https://github.com/NickvisionApps/Denaro). Since then app has been modified and updated on Github only. The app is developed in C# in Windows UI with Windows App SDK (WinUI 3 as at this time).

### Features Offered by Denaro

 * Manage multiple accounts simultaneously with its most popular and familiar tab interface
 * Filter transactions by type, group, or date
 * Repeat transactions such as bills that occur every month
 * Transfer money from one account to another
 * Export the data from an account as a CSV file and import a CSV, OFX or QIF file to add transactions to an account

## Denaro File Format - More Information

Denaro files are saved to disc in binary file format. Financial data is stored as a database file in **.SQLITE3** file format. SQLITE is a lightweight SQL database file created with the SQLite software. It provides self-contained database engine that is capable of providing fully featured and highly reliable database. SQLite database files can be used to share rich contents between systems by simply exchanging these files over the network. SQLite bindings exist for programming languages such as C, [C#](/programming/cs/), [C++](/programming/cpp/), [Java](/programming/java/), [PHP](/programming/php/), and many others.

## References

 * [Nickvision](https://nickvision.org/)
 * [NIckVision - Github](https://github.com/NickvisionApps/Denaro)
