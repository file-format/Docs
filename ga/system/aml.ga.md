{
  "date" : "2022-04-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Comhad AML - Comhad Teanga Meaisín ACPI",
  "description":"Foghlaim faoi fhormáid comhaid AML ACPI agus APIanna ar féidir leo comhaid AML a chruthú agus a oscailt.",
  "linktitle" : "AML",
  "menu" : {
    "docs" : {
      "identifier" : "system-aml-ga",
      "parent" : "system"
}
},
  "lastmod" : "2022-04-12"
}

## Cad is comhad AML ann?

Is comhad córais é comhad AML a cruthaíodh leis an teanga Ardchumraíochta agus Comhéadain Cumhachta (ACPI) a úsáidtear chun airíonna crua-earraí a chumrú. Tá cód beart neamhspleách meaisín ann a úsáidtear chun crua-earraí a chumrú fiú le haghaidh oibríochtaí simplí ar nós ríomhaire a mhúchadh. Féadfaidh treoracha a bheith i gcomhaid AML ag brath ar an gcuspóir a bhfuil sé le suiteáil ar an meaisín dó. Ligeann cur i bhfeidhm na gcaighdeán ACPI duit feidhmiúlacht bhainistíochta cumhachta agus comhéadan láidir a fheabhsú chun gléasanna máthairchláir ar nós na máthairchláir P55 a chumrú.

## Formáid Chomhaid ACPI AML

Déantar comhaid AML a shábháil mar chomhaid dhénártha ar diosca agus an t-ábhar scríofa i gcód beart. Tá na sonraíochtaí formáid comhaid de chaighdeán ACPI ar fáil ar [uefi](https://uefi.org/). Tá an teanga deartha chun cobhsaíocht agus cúl-chomhoiriúnacht a thairiscint, rud a éilíonn níos lú athscríobh nó ath-thógáil ar chruach na bhfeidhmchlár.

## Sonraíochtaí Formáid Comhaid AML

Cuimsíonn comhad AML táblaí DSDT agus SSDT. Déantar an cód beart AML a léamh agus a pharsáil ó thús gach ceann de na táblaí seo. Tugann sé seo faisnéis faoi na sainmhínithe ar ghléasanna agus réada in ainmspás ACPI. Trí úsáid a bhaint as an bhfaisnéis seo, is féidir leis an ateangaire AML liosta a ghiniúint de na gléasanna go léir atá ar fáil sa chóras, agus na hairíonna agus na feidhmeanna a dtacaítear leo.

### Sampla de Chód ASL le haghaidh DSDT

Seo a leanas sampla de chód ASL do DSDT.

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

## Tagairtí

* [ACPI AML]( https://wiki.osdev.org/AML)

* [DSDT]( https://wiki.osdev.org/DSDT)

* [SSDT]( https://wiki.osdev.org/SSDT )


