{
  "date" : "2021-06-21",
  "keywords" : [ "UDL", "extension", "udl file", "udl file format", "Database File Type", "Database File Format", "what is a udl file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description" : "Learn about UDL file format and APIs that can create and open UDL files.",
  "title" : "UDL - Microsoft Universal Data Link File",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
    }
  },
  "lastmod" : "2021-06-21"
}

## What is a UDL file?
The file with .udl extension is called Microsoft Universal Data Link file; specifying connection attributes; used by Windows apps to establish a connection with the database. The UDL file contains the connection string for an OLE DB data source; with username and password and essential connection string properties. To avoid directly specifying the properties by hand in a connection string, a Data Link Properties dialog box can be used to save connection information in a .udl file as an alternative.

## UDL File Format
Basically, a UDL (Universal Data Link) file is a simple text file that consists of a database connection string with particular attributes or properties. Once the UDL file is created, it can be tested by using SQL Server Management Studio to verify the connectivity.

### Connection string properties
Following properties can be set in a UDL to ensure the proper connectivity:

- **Server Name**:  location of the server where the database you want to access is located.
- **Authentication Options**
	- **Windows Authentication**: Authentication to SQL Server using the currently logged-in user's Windows account credentials.
	- **SQL Server Authentication**: Authentication using login ID and password.
	- **Active Directory - Integrated**: Integrated authentication with an Azure Active Directory identity; can also be used for Windows authentication to SQL Server.
	- **Active Directory - Password**: User ID and password authentication with an Azure Active Directory identity.
	- **Active Directory - Universal with MFA support**: Interactive authentication with an Azure Active Directory identity.
	- **Active Directory - Service Principal**: Authentication with an Azure Active Directory service principal.
- **Server SPN**: If you use a trusted connection, you can specify a service principal name (SPN) for the server.
- **User name**: Type the User ID to use for authentication when you sign in to the data source.
- **Password**: Type the password to use for authentication when you sign in to the data source.
- **Blank password**: When checked, enables the specified provider to use a blank password in the connection string.
- **Allow saving password**: Allows the password to be saved with the connection string.
- **Use strong encryption for data**: data that is passed through the connection will be encrypted.
- **Trust server certificate**: The server's certificate will be validated.
- **Database**: Database name that you want to access.
- **Attach a database file as a database name**: Specifies the name of the primary file for an attachable database.

## References ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Universal Data Link (UDL) configuration](https://docs.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)
