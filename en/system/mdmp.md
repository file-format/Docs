{
  "date" : "2022-08-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "MDMP File - Windows Minidump File Format",
  "description":"Learn about MDMP file format and APIs that can create and open MDMP files.",
  "linktitle" : "MDMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
    }
  },
  "lastmod" : "2022-08-19"
}

## What is an MDMP file?

An MDMP file is a memory dump of an application on Microsoft Windows that is created when the application closes abnormally or crashes. It contains information and data dumps that can be used to debug the cause of the crash. MDMP files are applicable on applications created by any platform such as Java, C++, .NET and others. In addition to MDMP, 

Applications that can open MDMP files include Microsoft Visual Studio Debugger.

## MDMP File Format

MDMP files are saved as binary files to disc and can be opened with Microsoft Visual Studio debugger. It contains the following information to help identify the reason for the crash.

 * Details of the Stop message, its parameters, and other data
 * List of loaded drivers
 * Processor context (PRCB) for the processor that stopped working
 * Process information and kernel context (EPROCESS) for the process that stopped
 * Process information and kernel context (ETHREAD) for the thread that stopped
 * Kernel-mode call stack for the thread that stopped

This information helps to find out what happened, fix the problem and prevent it from happening again.

### Analyze Minidump

Windows requires a paging file on the boot volume to create a memory dump file. The paging file is created on the boot volume and should be at least 2 megabytes (MB) in size. The dump file is created when an application crashes. In case of a second problem, a second small memory dump file is created while the previous one is kept preserved. The name of dump file is distinct to avoid any overwriting.

Windows keeps a list of all the memory dump files in the %SystemRoot%\Minidump folder. You can analyze MDMP files by running them in Visual Studio Debugger as listed in the steps below.

## How do I open an MDMP file in Visual Studio?

The following steps can be used to open an MDMP file in Visual Studio.

 * In Visual Studio, from the File menu, choose Open | Crash Dump .
 * Navigate to the dump file you want to open.
 * Select Open.

## Reference

* [How to read the small memory dump file that is created by Windows if a crash occurs](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)
