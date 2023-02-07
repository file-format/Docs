{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AIDL ファイル - Android インターフェイス定義言語ファイル",
  "description":"例と,AIDL ファイルを作成して開くことができる API を使用して,AIDL ファイル形式とは何かについて学びます。",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .AIDL ファイルとは?

AIDL (Android Interface Definition Language) ファイルを使用すると、Android 開発者は異なるアプリ間の通信を確立できます。プログラミング インターフェイスに基づいて、クライアントとサービスの両方がプロセス間通信 (IPC) を使用して通信することに同意します。 AIDL ファイルには、これらのインターフェースを定義するための [Java](/ja/programming/java/) ソース コードと、アプリ間の通信用のコントラクトが含まれています。

AIDL ファイルは、Google Android Studio または Microsoft Notepad や Notepad++ などの任意のテキスト エディターで開くことができます。

## AIDL ファイル形式 - 詳細情報

AIDL は、アプリ間の通信用のインターフェイスを含むテキスト ファイルです。 Android OS では、あるプロセスが別のプロセスのメモリにアクセスすることは許可されていません。これにより、プロセスはオブジェクトをプリミティブに分割して、基礎となるオペレーティング システムを理解し、開発者向けの通信構造のプロセスを確立します。

### AIDL でサポートされているデータ型は?

AIDL は、デフォルトで次のデータ型をサポートしています。

* Java プログラミング言語のすべてのプリミティブ型 (int、long、char、boolean など)
* 弦
* CharSequence
* リスト
* 地図

## AIDL ファイルの例

次に、AIDL ファイルの例を示します。

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
## 参考文献

* [Android インターフェイス定義言語 (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

