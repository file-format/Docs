{
  "date" : "2021-08-10",
  "keywords" :[".ova ファイル","ファイル形式",".ova ファイルとは","ファイル","ファイル拡張子"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :".ova ファイル形式とは何か,および ova ファイルを作成して開くことができる API について学びます。",
  "title" :"OVAファイル形式 - 仮想アプライアンスファイルを開く",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## .OVA オプション番号

OVA (Open Virtual Appliance) ファイルは、.tar アーカイブ形式を使用してアーカイブとして保存される OVF ディレクトリです。これは、仮想マシンで実行されるソフトウェアの配布用のファイルを含む仮想アプライアンス パッケージ ファイルです。 OVA パッケージには、[.ovf](/disc-and-media/ovf/) 記述子ファイル、証明書ファイル、オプションの [.mf](/programming/mf/) ファイル、およびその他の関連ファイルが含まれています。 OVA ファイルのメディア タイプは application/ovf です。

## OVA ファイル形式

前述のように、OVA ファイルは、OVF ディレクトリを使用して TAR ファイル形式で作成されるアーカイブ ファイルです。ファイル自体はバイナリ ファイルとして保存されます。 VMware、Microsoft、Oracle、Citrix などのほとんどの仮想化プラットフォームは、仮想マシンにロードされるイメージの詳細を含む記述子ファイルである OVF ファイルから仮想アプライアンスをインストールできます。

## OVA ファイルの利点

* OVA ファイルは圧縮されているため、ダウンロードを高速化できます。
* vSphere Client は、OVA ファイルをインポートする前に検証し、目的の宛先サーバーと互換性があることを確認します。アプライアンスが選択したホストと互換性がない場合、インポートできず、エラー メッセージが表示されます。
* OVA は、多層アプリケーションと複数の仮想マシンをカプセル化できます。

## 参考文献

* [OVA ファイル形式とテンプレート](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html)
※【OVFファイル形式仕様書】(https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

