{
  "date" : "2022-01-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "CMS File Format - Connection Manager Service Profile File",
  "description":"Learn about CMS file and APIs that can create and open CMS files.",
  "linktitle" : "CMS",
  "menu" : {
    "docs" : {
      "identifier": "misc-cms",
      "parent" : "misc"
    }
  },
  "lastmod" : "2022-01-12"
}

## What is a CMS file?

A CMS file is a data file that contains profile information used by Microsoft Windows Connection Manager. It lets remote users connect to a network using this profile information. Information stored inside a CMS file includes data about user's operating system and permissions that is used to establish a connection between a remote user and the network. CMS administrators use the Connection Manager Administrator Kit (CMAK) to generate CMS files.

## CMS File Format - More Information

CMS files are not found commonly on user machines. Since these are used specifically to allow remote users to a network, you will find these on computers that are used to connect to a company network or some specific purpose-build office. In most cases, it is used to connect to an organizational network such as  Virtual Private Network (VPN) that is dedicated to a company only. Being a network administrator, you will set up access to such a network with Connection Manager for allowing him to access the company network from a remote locaiton.

### What's insdie CMS?

A CMS profile file is created using Connection Manager and is packaged with other configuration files before being provided to remote user. These additional files may include a CMP and and an INF file that are packaged alongside in an [EXE](/executable/exe/) file. This complete package is provided to the remote user for connecting to the network.

## References

* [Understanding and configuring Windows Connection Manager](https://docs.microsoft.com/en-us/windows-hardware/drivers/mobilebroadband/understanding-and-configuring-windows-connection-manager)
