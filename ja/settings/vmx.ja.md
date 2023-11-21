{
"日付": "2023-06-08",
  "keywords": [
"vmx ファイル",
"vmx ファイルとは何ですか",
"vmx ファイルの例",
"vmx ファイルを開く方法",
"vmx ファイルには何が含まれていますか",
"vmx ファイルの形式は何ですか",
"ファイル",
"vmx ファイル拡張子",
"拡大"
],
  "author": {
"display_name": "シェキール・ファイズ"
},
"ドラフト": "偽",
"toc": true,
"title": "VMX ファイル形式 - VMware 仮想マシン構成ファイル",
  "description":"VMX 形式と,VMX ファイルを作成して開くことができる API について学びます。",
"リンクタイトル": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent":"設定"
}
},
"lastmod": "2023-06-08"
}

## .VMX ファイルとは何ですか?

VMX ファイルは、仮想マシン構成ファイルとも呼ばれ、仮想マシン (VM) の設定と構成を定義するために VMware 仮想化ソフトウェアによって使用されるプレーン テキスト ファイルです。 VMX ファイルには、VM のハードウェア構成、仮想ディスク マッピング、ネットワーク設定、その他のパラメーターなどの情報が含まれています。

## VMX ファイルの例

VMX ファイルの例を次に示します。

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

## VMX ファイルには何が含まれていますか?

VMX ファイルには、仮想マシン (VM) のさまざまな構成設定が含まれています。 VMX ファイルでよく見られる設定の一部を次に示します。

- `.encoding:` ファイルで使用される文字エンコーディングを指定します。
- `config.version:` VMX ファイル形式のバージョンを示します。
- `virtualHW.version:` VM の仮想ハードウェアのバージョンを指定します。
- `guestOS:` VM にインストールされているゲスト オペレーティング システムを指定します。
- `memSize:` VM に割り当てられるメモリの量を定義します。
- `displayName:` VM の表示名またはラベルを設定します。
- `powerType:` さまざまな操作 (電源オフ、電源オン、リセット、サスペンド) の電源動作を定義します。
- `floppyX:` プレゼンスやファイル マッピングなど、フロッピー ドライブに関連する構成設定。
- `numvcpus:` VM に割り当てられる仮想 CPU の数を指定します。
- `scsiX:` SCSI コントローラとそれに関連する仮想ディスクの構成設定。
- `ethernetX:` 仮想デバイス タイプ、ネットワーク名、アドレス タイプなどのネットワーク アダプタの構成設定。
- `ideX:` IDE コントローラとそれに関連付けられた仮想ディスクの構成設定。
- `usbX:` 存在や接続の詳細など、USB デバイスの構成設定。
- `sound:` 仮想サウンド アダプターの構成設定。
- `tools.syncTime:` ホスト システムとの時刻同期が有効かどうかを示します。
- `uuid.bios:` VM の BIOS UUID を指定します。
- `uuid.location:` VM の場所の UUID を指定します。

## VMXファイルを開くにはどうすればよいですか?

VMX ファイルを手動で開くことはお勧めできません。 VMware Fusion を使用して仮想マシンを実行すると、ソフトウェアは VMX ファイルから情報を自動的にロードします。

ただし、VMX ファイルを手動で編集したい場合は、メモ帳 (Windows) や TextEdit (Mac) などのテキスト エディタを使用して編集できます。

## VMXファイルの形式は何ですか?

VMX ファイルは、特定の形式のプレーン テキスト ファイルです。形式はキーと値のペアの構造に従い、各行が個別の構成オプションを表します。

VMX ファイルの一般的な形式は次のとおりです。

```
key1 = value1
key2 = value2
key3 = value3
```

各行は、キーとそれに続く等号 (=) および対応する値で構成されます。キーは特定の構成設定を表し、値はその設定に割り当てられた値を表します。

たとえば、VMX ファイルの「memSize = "8192"」は、仮想マシンのメモリ制限が 8192MB の RAM であることを指定します。

VMX ファイルの形式には、行の先頭にポンド記号 (#) で示されるコメントが含まれる場合もありますが、ファイルの解析時に VMware ソフトウェアによって無視されます。コメントは、特定の設定に関する追加情報や説明を提供するためによく使用されます。

## 参考文献
* [サンプル VMX ファイル](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




