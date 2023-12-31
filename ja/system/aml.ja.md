{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AML ファイル - ACPI 機械語ファイル",
  "description":"ACPI AML ファイル形式と,AML ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## .AML ファイルとは?

AML ファイルは、ハードウェア プロパティの構成に使用される Advanced Configuration and Power Interface (ACPI) 言語で作成されたシステム ファイルです。これには、コンピューターのシャットダウンなどの単純な操作でもハードウェアを構成するために使用される、マシンに依存しないバイト コードが含まれています。 AML ファイルには、マシンにインストールする目的に応じた指示が含まれている場合があります。 ACPI 標準の実装により、電源管理機能と、P55 マザーボードなどのマザーボード デバイスを構成するための堅牢なインターフェイスを強化できます。

## ACPI AML ファイル形式

AML ファイルはバイナリ ファイルとしてディスクに保存され、コンテンツはバイト コードで書き込まれます。 ACPI 標準のファイル形式仕様は [uefi](https://uefi.org/) で入手できます。この言語は、安定性と下位互換性を提供するように設計されており、アプリケーション スタックの再書き込みや再構築が少なくて済みます。

## AML ファイル形式の仕様

AML ファイルは、DSDT および SSDT テーブルで構成されます。 AML バイト コードは、これらの各テーブルの先頭から読み取られて解析されます。これにより、ACPI 名前空間のデバイスとオブジェクトの定義に関する情報が得られます。この情報を使用して、AML インタープリターは、システムで使用可能なすべてのデバイスと、それらのサポートされているプロパティおよび機能のリストを生成できます。

### DSDT の ASL コードの例

DSDT の ASL コードの例は次のとおりです。

```
DefinitionBlock ("test.aml", "DSDT", 1, "OEMID ", "TABLEID  ", 0x00000000)
{
    Scope (_SB)
    {
        Device (PCI0)
        {
            Name (_HID, EisaId ("PNP0A03"))
    }
}
}
```

## 参考文献

* [ACPI AML](https://wiki.osdev.org/AML)
* [DSDT](https://wiki.osdev.org/DSDT)
* [SSDT](https://wiki.osdev.org/SSDT)

