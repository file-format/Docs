{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
  },
  "draft": "false",
  "toc": true,
  "title": "LOCK File Format - What is a Lock file?",
  "description": "Learn about the LOCK file format and its .",
  "linktitle": "LOCK",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-lock"
    }
  },
  "lastmod": "2022-01-26"
}

## What is a LOCK file?

A **LOCK** file is a renamed file that is used by applications and operating systems to mark a file or some device as locked. This tells other applications not to use the file unless it is free from the application that is using it. In most of the cases, these lock files are empty, but in other cases, they may contain information related to the lock such as properties and settings.

Sometimes, the .lock file is is used by Microsoft's .NET Framework to create **lockeed** copies of a database file. In such a case, a copy of the database file will open with .lock extension. This doesn't allow the user to make changes to the file while it is in use by another user.

## LOCK File Format - More Information

A LOCK file is created by each application and its file format is specific to the application. These lock files can be saved in both text as well as binary file format.

The presence of lock files prevents simultaneous access of a resource to multiple files trying to access that resource. A copy of the original file is created with .lock extension suffixed to its name. This tells other applications to have read-only access to the file. For example, resource.dat will become resource.data.lock.

For Ruby programming language, you may come across the file **gemfile.lock**. This is where Bundler keeps record of the exact versions that were installed. Thus, when a project/library is moved to another machine, running bundle will look at the Gemfile for the exact relevant version.

## Lock File in Linux

Linux supports two types of file locks: advisory locks and mandatory locks.

 * **Advisory Locks**: Type of locking that is not enforced. In this case, participating processes cooperate with each other explicitly acquiring locks. If this is not possible, advisory locks are ignored.

 * **Mandatory Locks**: In case of Mandatory locking, the operating system enforces the file locking by preventing other processes from reading or writing the file. This does not require any cooperation between the processes.

 mandatory locking doesn’t require any cooperation between the participating processes. Once a mandatory lock is activated on a file, the operating system prevents other processes from reading or writing the file.

## References

* [GemFile and Gemfile.lock in Ruby](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Locking in Linux](https://www.baeldung.com/linux/file-locking)
