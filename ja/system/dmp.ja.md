{
  "date" : "2021-07-07",
  "keywords" :["DMP","拡張子","ファイル","フォーマット","システム","MemoryDump","ミニダンプ","プログラム","コンピューター","アプリケーション"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump ファイル形式",
  "description":"DMP ファイル形式と,DMP ファイルを作成して開くことができる API について学びます。",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## .DMP オプション番号##

DMP ファイルは、主に MemoryDump または Minidump ファイル形式に関連付けられています。これは、Microsoft Windows オペレーティング システムで、コンピューターのメモリ空間からダンプされたデータを格納するために使用されます。通常、DMP ファイルは、ファイルがクラッシュしたりエラーが発生したりすると作成されます。 DMP ファイルは、技術専門家や上級コンピュータ ユーザーが直面している問題をトラブルシューティングし、あらゆる種類のアプリケーションの問題を解決するために非常に重要な場合があります。 DMP ファイルは、システムにインストールされているアプリケーションをデバッグするためにオペレーティング システムによって使用される Microsoft 独自の形式として保存されます。


## DMP ファイル形式の技術仕様

Windows では、「savedump.exe」システム ツールが .dmp ファイルを生成します。このファイルは、利用可能なさまざまなデバッグ ユーティリティで処理できます。ミニ ダンプ (64/128 Kb) は、Windows によって '%SystemRoot%\Minidump' ディレクトリに保存されます。一方、カーネル メモリとフル メモリ ダンプは、システム ルートに「Memory.dmp」ファイルとして保存されます。メモリ ダンプ ファイルは比較的大きなファイルであるため、十分な量のストレージ スペースが必要になる場合があります。したがって、問題のトラブルシューティングには役に立たないと思われる不要な .dmp ファイルは削除することをお勧めします。

.dmp ファイルは、手動で削除するか、コンピュータのデフォルトの「ディスク クリーン ウィザード」を使用して削除できます。 DMP 拡張機能は、作成および使用されるバックアップおよびリカバリ データベース ファイルで .dmp ファイルを使用するために、Oracle データベース製品によって使用されます。 Oracle によって作成された DMP ファイルは、データベース サーバーを介して実行中のデータベース インスタンスにインポートまたは復元するために使用できるデータベース バックアップです。ほとんどの場合、.dmp ファイルにはファイル名として時刻と日付のスタンプがあります。

### DMP ファイルの内容

メモリ ダンプ ファイルには次のものが含まれます。

* stop ステートメントとそのパラメーター。
* ロードされたドライバーのリスト。
* Windows の通常の動作を停止させたプロセスのプロセッサ コンテキスト (PRCB)。
* 停止されたプロセスのカーネル コンテキストとプロセッサ情報 (EPROCESSES)。
* 停止したスレッドのカーネル コンテキストとプロセッサ情報 (ETHREAD)。
* プロセスの実行を終了したスレッドのカーネル モード コール スタック。


## DMP の例

停止エラー 0XC0000218 (Registry_File_Failure) は、次のように DMP ファイルを作成します。

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## 参照 ＃＃

* [DMP - マイクロソフト](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

