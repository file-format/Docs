{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LOCK 文件格式 - 什么是 Lock 文件？",
  "description":"了解 LOCK 文件格式及其 .",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## 什么是 .LOCK 文件？

**LOCK** 文件是重命名的文件，应用程序和操作系统使用它来将文件或某些设备标记为已锁定。这告诉其他应用程序不要使用该文件，除非它从正在使用它的应用程序中释放出来。在大多数情况下，这些锁文件是空的，但在其他情况下，它们可能包含与锁相关的信息，例如属性和设置。

有时，Microsoft 的 .NET Framework 使用 .lock 文件来创建数据库文件的 **lockeed** 副本。在这种情况下，数据库文件的副本将以 .lock 扩展名打开。这不允许用户在其他用户使用文件时对其进行更改。

## LOCK 文件格式 - 更多信息

LOCK 文件由每个应用程序创建，其文件格式特定于应用程序。这些锁定文件可以以文本和二进制文件格式保存。

锁定文件的存在阻止了一个资源同时访问多个试图访问该资源的文件。创建原始文件的副本，其名称后缀为 .lock 扩展名。这告诉其他应用程序对该文件具有只读访问权限。例如，resource.dat 将变为 resource.data.lock。

对于 Ruby 编程语言，您可能会遇到文件 **gemfile.lock**。这是 Bundler 记录已安装的确切版本的地方。因此，当一个项目/库被移动到另一台机器上时，运行包将查看 Gemfile 以获得确切的相关版本。

## 在 Linux 中锁定文件

Linux 支持两种类型的文件锁：建议锁和强制锁。

* **咨询锁**：未强制执行的锁定类型。在这种情况下，参与的进程相互合作，显式地获取锁。如果这是不可能的，建议锁将被忽略。

* **强制锁定**：在强制锁定的情况下，操作系统通过阻止其他进程读取或写入文件来强制执行文件锁定。这不需要进程之间的任何合作。

强制锁定不需要参与进程之间的任何合作。一旦在文件上激活强制锁定，操作系统就会阻止其他进程读取或写入文件。

## 参考

* [Ruby 中的 GemFile 和 Gemfile.lock](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)
* [Linux 中的锁定](https://www.baeldung.com/linux/file-locking#:~:text=File%20locking%20is%20a%20mechanism,very%20dangerous%20command%20in%20Linux.)

