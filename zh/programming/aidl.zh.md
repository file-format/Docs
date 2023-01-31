{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL 文件——Android 接口定义语言文件",
  "description":"通过示例和可以创建和打开 AIDL 文件的 API 了解什么是 AIDL 文件格式。",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .AIDL 文件是什么？

AIDL（Android 接口定义语言）文件允许 Android 开发人员在不同的应用程序之间建立通信。基于编程接口，客户端和服务都同意使用进程间通信 (IPC) 进行通信。 AIDL 文件包含 [Java](/zh/programming/java/) 源代码，用于定义应用程序之间通信的这些接口和契约。

您可以使用 Google Android Studio 或任何文本编辑器（如 Microsoft Notepad 和 Notepad++）打开 AIDL 文件。

## AIDL 文件格式 - 更多信息

AIDL 是包含应用程序之间通信接口的文本文件。 Android 操作系统不允许一个进程访问另一个进程的内存。这导致进程将它们的对象拆分为原语以了解底层操作系统并为开发人员建立通信结构的进程。

### AIDL 支持哪些数据类型？

AIDL 默认支持以下数据类型。

* Java编程语言中的所有原始类型（如int、long、char、boolean等）
* 细绳
* 字符序列
* 列表
* 地图

## AIDL 文件示例

以下是一个示例 AIDL 文件。

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## 参考

* [Android 接口定义语言 (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

