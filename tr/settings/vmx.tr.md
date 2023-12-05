{
"tarih": "2023-06-08",
  "keywords": [
"vmx dosyası",
"vmx dosyası nedir",
"vmx dosyası örneği",
"vmx dosyası nasıl açılır",
"vmx dosyası neler içerir",
"vmx dosyasının formatı nedir",
"dosya",
"vmx dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "VMX Dosya Formatı - VMware Sanal Makine Yapılandırma Dosyası",
  "description":"VMX dosyalarını oluşturabilen ve açabilen VMX formatı ve API'ler hakkında bilgi edinin.",
"linktitle" : "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"sonmod": "2023-06-08"
}

## .VX dosyası nedir?

Sanal makine yapılandırma dosyası olarak da bilinen VMX dosyası, VMware sanallaştırma yazılımı tarafından sanal makinenin (VM) ayarlarını ve yapılandırmasını tanımlamak için kullanılan bir düz metin dosyasıdır. VMX dosyaları VM'nin donanım yapılandırması, sanal disk eşlemeleri, ağ ayarları ve diğer parametreler gibi bilgileri içerir.

## VMX Dosya Örneği

VMX dosyasının nasıl görünebileceğine dair bir örnek:

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

## VMX dosyası ne içeriyor?

Bir VMX dosyası, sanal makine (VM) için çeşitli yapılandırma ayarlarını içerir. VMX dosyasında yaygın olarak bulunan ayarlardan bazıları şunlardır:

- `.encoding:` Dosyada kullanılan karakter kodlamasını belirtir.
- `config.version:` VMX dosya biçiminin sürümünü belirtir.
- `virtualHW.version:` VM için sanal donanımın sürümünü belirtir.
- `guestOS:` VM'de yüklü konuk işletim sistemini belirtir.
- `memSize:` VM'ye ayrılan bellek miktarını tanımlar.
- `displayName:` VM için görünen adı veya etiketi ayarlar.
- `powerType:` Farklı işlemler için güç davranışını tanımlar (güç kapatma, açma, sıfırlama, askıya alma).
- `floppyX:` Disket sürücüleriyle ilgili, mevcudiyet ve dosya eşlemeleri gibi yapılandırma ayarları.
- `numvcpus:` VM'ye atanan sanal CPU sayısını belirtir.
- `scsiX:` SCSI denetleyicileri ve bunlarla ilişkili sanal diskler için yapılandırma ayarları.
- `ethernetX:` Sanal aygıt türü, ağ adı ve adres türü de dahil olmak üzere ağ bağdaştırıcıları için yapılandırma ayarları.
- `ideX:` IDE denetleyicileri ve bunlarla ilişkili sanal diskler için yapılandırma ayarları.
- `usbX:` USB aygıtları için iletişim durumu ve bağlantı ayrıntıları gibi yapılandırma ayarları.
- `ses:` Sanal ses bağdaştırıcısının yapılandırma ayarları.
- `tools.syncTime:` Ana bilgisayar sistemiyle zaman senkronizasyonunun etkin olup olmadığını gösterir.
- `uuid.bios:` VM'nin BIOS UUID'sini belirtir.
- `uuid.location:` VM'nin konum UUID'sini belirtir.

## VMX dosyası nasıl açılır?

VMX dosyasının manuel olarak açılması önerilmez. VMware Fusion kullanarak bir sanal makine çalıştırdığınızda yazılım, bilgileri VMX dosyasından otomatik olarak yükler.

Ancak, VMX dosyasını manuel olarak düzenlemek istiyorsanız bunu herhangi bir metin düzenleyiciyi (örneğin, Not Defteri (Windows) veya TextEdit (Mac) kullanarak yapabilirsiniz.

## VMX dosyasının formatı nedir?

VMX dosyası, belirli formatta düz bir metin dosyasıdır. Format, her satırın ayrı bir konfigürasyon seçeneğini temsil ettiği bir anahtar-değer çifti yapısını takip eder.

VMX dosyasının genel formatı aşağıdaki gibidir:

```
key1 = value1
key2 = value2
key3 = value3
```

Her satır, anahtarın ardından eşittir işareti (=) ve karşılık gelen değerden oluşur. Anahtar, belirli bir yapılandırma ayarını temsil eder ve değer, bu ayara atanan değeri temsil eder.

Örneğin, VMX dosyasındaki `memSize = "8192"`, Sanal Makine bellek sınırının 8192 MB RAM olduğunu belirtir.

VMX dosyasının formatı, satırın başında kare işareti (#) ile gösterilen ve dosya ayrıştırılırken VMware yazılımı tarafından göz ardı edilen yorumları da içerebilir. Yorumlar genellikle belirli ayarlara ilişkin ek bilgi veya açıklamalar sağlamak için kullanılır.

## Referanslar
* [Örnek VMX Dosyası](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




