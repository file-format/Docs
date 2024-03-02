{
  "date": "2023-06-08",
  "keywords": [
"comhad vmx",
"Cad is comhad vmx",
"Sampla comhad vmx",
"Conas a oscailt comhad vmx",
"Cad atá i gcomhad vmx",
"Cad é formáid an chomhaid vmx",
"comhad",
"Síneadh comhad vmx",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid VMX - Comhad Cumraíochta Meaisín Fíorúil VMware",
  "description": "Foghlaim faoi fhormáid VMX agus APIs ar féidir leo comhaid VMX a chruthú agus a oscailt.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx-ga",
      "parent": "settings"
}
},
  "lastmod": "2023-06-08"
}

## Cad is comhad VMX ann?

Is comhad gnáth-théacs é comhad VMX, ar a dtugtar comhad cumraíochta meaisín fíorúil freisin, a úsáideann bogearraí fíorúlaithe VMware chun socruithe agus cumraíocht an mheaisín fíorúil (VM) a shainiú. Cuimsíonn comhaid VMX faisnéis ar nós cumraíocht crua-earraí VM, mapálacha diosca fíorúil, socruithe líonra agus paraiméadair eile.

## Sampla Comhad VMX

Seo sampla den chuma a bheadh ar chomhad VMX:

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

## Cad atá i gcomhad VMX?

Tá socruithe cumraíochta éagsúla le haghaidh meaisín fíorúil (VM) i gcomhad VMX. Seo cuid de na socruithe a fhaightear go coitianta i gcomhad VMX:

- `.ionchódú:` Sonraítear an t-ionchódú carachtar a úsáidtear sa chomhad.
- `config.version:` Léiríonn an leagan den fhormáid comhaid VMX.
- `virtualHW.version:` Sonraítear leagan na crua-earraí fíorúla don VM.
- `guestOS:` Sonraítear an córas oibriúcháin aoi atá suiteáilte sa VM.
- `memSize:` Sainmhíníonn sé an méid cuimhne a leithdháileadh ar an VM.
- `displayName:` Socraíonn sé an t-ainm taispeána nó an lipéad don VM.
- `powerType:` Sainmhíníonn sé an t-iompar cumhachta le haghaidh oibríochtaí éagsúla (cumhacht as, cumhacht ar, athshocrú, fionraí).
- `floppyX:` Socruithe cumraíochta a bhaineann le tiomántáin flapacha, amhail láithreacht agus mapálacha comhaid.
- `numvcpus:` Sonraítear líon na LAPanna fíorúla a shanntar don VM.
- `scsiX:` Socruithe cumraíochta do rialtóirí SCSI agus na dioscaí fíorúla a bhaineann leo.
- `ethernetX:` Socruithe cumraíochta d'oiriúnóirí líonra, lena n-áirítear cineál an ghléis fhíorúil, ainm líonra agus cineál seoltaí.
- `ideX:` Socruithe cumraíochta do rialtóirí IDE agus na dioscaí fíorúla a bhaineann leo.
- `usbX:` Socruithe cumraíochta do ghléasanna USB, amhail sonraí láithreachta agus naisc.
- `fuaim:` Socruithe cumraíochta don oiriúntóir fuaime fíorúil.
- `tools.syncTime:` Léiríonn sé an bhfuil sioncrónú ama leis an gcóras óstaigh cumasaithe.
- `uuid.bios:` Sonraítear UUID BIOS an VM.
- `uuid.location:` Sonraíonn sé suíomh UUID an VM.

## Conas comhad VMX a oscailt?

Ní mholtar comhad VMX a oscailt de láimh. Nuair a ritheann tú meaisín fíorúil ag baint úsáide as VMware Fusion, lódálann na bogearraí an fhaisnéis ón gcomhad VMX go huathoibríoch.

Mar sin féin, más mian leat comhad VMX a chur in eagar de láimh, is féidir leat é sin a dhéanamh trí úsáid a bhaint as aon eagarthóir téacs m.sh. Notepad (Windows) nó TextEdit (Mac).

## Cad é formáid an chomhaid VMX?

Is comhad gnáth-théacs é comhad VMX le formáid ar leith. Leanann an fhormáid struchtúr péire eochairluacha ina léiríonn gach líne rogha cumraíochta ar leith.

Seo a leanas formáid ghinearálta an chomhaid VMX:

```
key1 = value1
key2 = value2
key3 = value3
```

Tá eochair i ngach líne agus comhartha comhionann (=) agus luach comhfhreagrach ina dhiaidh sin. Seasann an eochair do shocrú cumraíochta ar leith agus seasann an luach don luach a shanntar don socrú sin.

Mar shampla, sonraíonn `memSize=8192` i gcomhad VMX gurb é 8192MB RAM an teorainn chuimhne Meaisín Fíorúil.

D’fhéadfadh go n-áireofaí i bhformáid comhaid VMX tráchtanna freisin, arna sonrú ag comhartha punt (#) ag tús na líne, a dtugann bogearraí VMware neamhaird orthu agus an comhad á pharsáil. Is minic a úsáidtear tuairimí chun faisnéis nó mínithe breise a sholáthar do shuíomhanna sonracha.

## Tagairtí
* [Comhad VMX Sampla](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)





