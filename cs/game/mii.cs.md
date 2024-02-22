{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Přečtěte si o formátu souboru Age of Empires 2 Expansion Replay MGX a rozhraních API, která mohou vytvářet a otevírat soubory MGX.",
  "title" : "Soubor MII – formát souboru virtuálního avataru pro Wii",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-cs",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Co je soubor MII?

Soubor MII je formát souboru virtuálního avatara, který se používá k ukládání virtuálních avatarů na herní konzoli Nintendo Wii. Tyto soubory obsahují informace, jako je vzhled, pohyby a animace avatara. Lze je použít ve hrách, aplikacích sociálních sítí a dalším softwaru na Wii. Soubor MII obsahuje také další funkce o avatarovi, jako je pohlaví, barva vlasů, barva pleti, rysy obličeje a typ očí.

Soubor MII můžete otevřít pomocí [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## Formát souboru MII

Formát souboru MII je podrobně definován na [Wii Brew](https://wiibrew.org/wiki/Mii_data). Řetězce v souboru MII jsou uloženy ve formátu Unicode (UTF-16), big-endian.

### Blok MI

Data souboru MII jsou uložena na Wiimote ve dvou blocích. Každý blok je dlouhý 750 bajtů, s 2bajtovým CRC, což činí celkem 752 bajtů. Každý blok začíná 4bajtovou hodnotou ('RNCD'), která se zdá být magickým číslem pro formát souboru MII.

## Jak vytvořit MII soubory?

Existuje několik různých způsobů, jak vytvořit avatary pro Nintendo Wii:

1. `Pomocí vestavěného kanálu Mii na Wii:` Tento kanál vám umožňuje vytvářet vlastní avatary pomocí různých nástrojů, včetně rysů obličeje, tvaru těla a oblečení. Jakmile vytvoříte svého avatara, můžete jej uložit jako soubor Mii a použít jej ve hrách a dalším softwaru na Wii.

1. `Používání aplikace Mii Maker na Nintendu 3DS:` Aplikace Mii Maker umožňuje vytvářet vlastní avatary pomocí dotykové obrazovky a fotoaparátu na Nintendu 3DS. Jakmile vytvoříte svého avatara, můžete jej uložit jako soubor Mii a přenést jej do svého Wii prostřednictvím bezdrátového připojení.

1. `Použití softwaru třetích stran:` Někteří vývojáři vytvořili software, který vám umožňuje vytvářet vlastní avatary pro Wii. Tento software je obvykle navržen pro použití na počítači a může vyžadovat další kroky k přenosu avatara do vašeho Wii.

1. `Používání předem vytvořených avatarů:` Některé hry a další software na Wii mohou být dodávány s předem připravenými avatary, které můžete použít.

Ve všech případech musíte mít účet Nintendo k vytvoření a uložení svého avatara na Wii.

## Reference

* [Editor mého avataru](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


