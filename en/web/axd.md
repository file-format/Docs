{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "AXD File - ASP.NET Web Handler File Format",
  "description" : "Learn about what is an AXD file and APIs that can create and open AXD files.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
    }
  },
  "lastmod" : "2023-05-23"
}

## What is an AXD file?

An AXD file is a web settings file that is used for handling and retrievign embedded resource requests in ASP.NET. It comprises of instructions for retreiving embedded resources such as images, JavaScript ([.JS](/web/js/)) files, and [.CSS](/web/css/) files. AXD files are used for injecting resources into client-side pages. This allows client pages to access these resources on server in a standard way.

## AXD File Format

AXD files are stored as binary files on server side. It refers to a Web Handler file in ASP.NET which are components that generate responses to specific requests to a web server. AXD files perform custom processing before generating the response based on client-side page requests. These are typically saved as **WebResource.axd** files.

### What is WebResource.axd file?

Most ASP.NET projects save AXD files as WebResource.axd files that allow client-side pages to download resources that are embeddedin an assembly. Your application may face slow performance in case you run it in debug mode as WebResources.axd handler is not cached.

## References

 * [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)
