{
  "date": "2023-06-08",
  "keywords": [
    "vmx file",
    "what is a vmx file",
    "vmx file example",
    "how to open vmx file",
    "what does vmx file contain",
    "what is the format of vmx file",
    "file",
    "vmx file extension",
    "extension"
  ],
  "author": {
    "display_name": "Shakeel Faiz"
  },
  "draft": "false",
  "toc": true,
  "title": "VMX File Format - VMware Virtual Machine Configuration File",
  "description": "Learn about VMX format and APIs that can create and open VMX files.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
    }
  },
  "lastmod": "2023-06-08"
}

## What is a VMX file?

A VMX file, also known as virtual machine configuration file, is a plain text file used by VMware virtualization software to define settings and configuration of virtual machine (VM). VMX files contain information such as VM's hardware configuration, virtual disk mappings, network settings and other parameters.

## VMX File Example

Here is an example of what VMX file might look like:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## What does VMX file contain?

A VMX file contains various configuration settings for virtual machine (VM). Here are some of the commonly found settings in VMX file:

- `.encoding:` Specifies the character encoding used in the file.
- `config.version:` Indicates the version of the VMX file format.
- `virtualHW.version:` Specifies the version of the virtual hardware for the VM.
- `guestOS:` Specifies the guest operating system installed in the VM.
- `memSize:` Defines the amount of memory allocated to the VM.
- `displayName:` Sets the display name or label for the VM.
- `powerType:` Defines the power behavior for different operations (power off, power on, reset, suspend).
- `floppyX:` Configuration settings related to floppy drives, such as presence and file mappings.
- `numvcpus:` Specifies the number of virtual CPUs assigned to the VM.
- `scsiX:` Configuration settings for SCSI controllers and their associated virtual disks.
- `ethernetX:` Configuration settings for network adapters, including the virtual device type, network name, and address type.
- `ideX:` Configuration settings for IDE controllers and their associated virtual disks.
- `usbX:` Configuration settings for USB devices, such as presence and connection details.
- `sound:` Configuration settings for the virtual sound adapter.
- `tools.syncTime:` Indicates whether time synchronization with the host system is enabled.
- `uuid.bios:` Specifies the BIOS UUID of the VM.
- `uuid.location:` Specifies the location UUID of the VM.

## How to open VMX file?

Opening a VMX file manually is not recommended. When you run a virtual machine using VMware Fusion, the software automatically loads the information from the VMX file.

However, if you want to manually edit VMX file, you can do so using any text editor e.g. Notepad (Windows) or TextEdit (Mac).

## What is the format of VMX file?

A VMX file is a plain text file with specific format. The format follows a key-value pair structure where each line represents separate configuration option.

The general format of VMX file is as follows:

```
key1 = value1
key2 = value2
key3 = value3
```

Each line consists of key followed by equal sign (=) and corresponding value. The key represents a specific configuration setting and the value represents the value assigned to that setting.

For example, `memSize = "8192"` in VMX file specifies that Virtual Machine memory limit is 8192MB of RAM.

The format of VMX file may also include comments, denoted by a pound sign (#) at the beginning of the line, which are ignored by VMware software when parsing the file. Comments are often used to provide additional information or explanations for specific settings.

## References
* [Sample VMX File](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)



