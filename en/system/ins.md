{
  "date" : "2021-07-16",
  "keywords" : [ "ins file", "ins file format", "what is an ins file", "file", "ins example", "ins file extension","extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about INS file format and APIs that can create and open INS files.",
  "title" : "INS - Internet Settings File",
  "linktitle" : "INS",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2021-07-16"
}

## What is an INS file?

The file with .ins extension is generally used by Microsoft Windows for setting up dial-up and broadband Internet connections. Actually, it contains connection setup information that allows Windows to set up Internet access to an ISP. An INS file is commonly used for setting up Internet Explorer (IE) LAN connection settings. The IE connection settings files sometimes provided by the ISPs and system administrators to the users with a URL to the INS file. 

## INS file format
You can use the Internet Settings files (INS) along with the Internet Explorer Administration Kit 11 (IEAK 11) to configure your custom browser and its components. You can write various versions of your custom package by customizing copies of the INS file.

### Possible INS Settings
The possible INS settings are given in the following table:

| Setting | Description |
-----|---------|
| URL | Whether to use an auto-configured proxy server. |
| Branding | Customize the branding and setup information in your browser package. |
| Media | Types of media in which your custom installation package is available. |
| BrowserToolbars | Customize the appearance of the IE toolbar. |
| CabSigning | Digital signature information for your programs. |
| HideCustom | Whether to hide the globally unique identifier (GUID) for each custom component. |
| ConnectionSettings | Info about the networking connection settings used to install your custom package. |
| CustomBranding | URL location to your branding cabinet (.cab) file. |
| ExtRegInf | Names of your Setup information (.inf) files and the installation mode for components. |
| FavoritesEx | Add a path to your icon file for Favorites, decide whether Favorites are available offline, and add URLs to eachFavorites site. |
| ISP_Security | The root certificate you’re adding to your custom package. |
| Proxy | Whether to use a proxy server. |
| Security Imports | Whether to import security information for your custom package. |




## References 

* [Using Internet Settings (.INS) files with IEAK 11](https://learn.microsoft.com/en-us/internet-explorer/ie11-ieak/using-internet-settings-ins-files)

