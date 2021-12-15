
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "ABC - ActionScript Byte Code File",
  "description":"Learn about what is ABC file format with example and APIs that can create and open ABC files.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2021-12-14"
}

## What is an ABC file?

A file with .abc extension is an ActionScript Byte Code File created by Flash compiler as a result of compiling the ActionScript script files. The byte code contained in the ABC file is executed by the [ActionScript Virtual Machine](https://www.adobe.com/content/dam/acom/en/devnet/pdf/avm2overview.pdf) (AVM and AVM2). The byte code comprises of constant data, instructions from the AVM2 instruction set, and various kinds of metadata. When an ABC file is loaded into the AVM or AVM2, it undergoes verification. If it does not conform to the AVM2 Overview, it is rejected. ABC files can be opened in Adobe Flash Player that has been discontinued long time ago.

## ABC File Format - More Information

ABC files are saved to disc in binary file format that are readable by AVM or AVM2 virtual machines. Its internal file structure represents executable code block with all its constant data, type descriptors, code, and metadata.

## ABC File Structure

ABC file structure is as shown below.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### ABC File Fields

|Field Name|Description|
---|---|
|minor_version, major_version|The values of major_version and minor_version are the major and minor version numbers of the abcFile format.|
|constant_pool|The constant_pool is a variable length structure composed of integers, doubles, strings, namespaces, namespace sets, and multinames.|
|method_count, method|The value ofmethod_count is the number of entries in the method array.   Each entry in the method array is a variable length method_info structure.|
|metadata_count, metadata|The value of metadata_count is the number of entries in the metadata array.  Each metadata entry is a metadata_infostructure that maps a name to a set of string values. |
|class_count, instance, class|The value of class_count is the number of entries in the instance and class arrays. |
|script_count, script|The value of script_count is the number of entries in the script array.  Each script entry is a script_info structure that defines the characteristics of a single script in this file. |
|method_body_count, method_body|The value of method_body_count is the number of entries in the method_body array.  Each method_bodyentry consists of a variable length method_body_info structure which contains the instructions for an individual method or function.|

## References

 * [Robust ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)
