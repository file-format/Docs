{
  "date": "2023-06-08",
  "keywords": [
"hpp comhad",
"Cad is comhad hpp ann",
"Cad atá sa chomhad hpp",
"Comhad hpp mar shampla",
"Cad é formáid an chomhaid hp",
"comhad",
"Síneadh comhad hp",
"síneadh"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "Formáid Comhaid HPP - Comhad Ceanntásca C++",
  "description": "Foghlaim faoi fhormáid HPP agus APInna ar féidir leo comhaid HPP a chruthú agus a oscailt.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp-ga",
      "parent": "programming"
}
},
  "lastmod": "2023-06-08"
}

## Cad is comhad HPP ann?

Úsáidtear an fhormáid comhaid .hpp go coitianta le haghaidh comhad ceanntásca i dteanga ríomhchlárúcháin C++. De ghnáth bíonn dearbhuithe agus sainmhínithe ar fheidhmeanna, aicmí, athróga agus tairisigh a úsáideann comhaid cód foinse eile i dtionscadal C++ i gcomhaid cheanntásc.

Is é an cuspóir atá le comhaid ceanntásc a úsáid ná bealach a sholáthar chun cód coiteann a roinnt ar fud comhaid cód foinse iolracha gan an cód féin a dhúbailt. Nuair is gá do bhunchomhad C++ rochtain a fháil ar dhearbhuithe nó ar shainmhínithe ón gcomhad ceanntásca, áirítear ann an comhad ceanntásca ag baint úsáide as treoir réamhphróiseálaí `# cuir san áireamh`.

Is minic a úsáidtear an síneadh comhad .hpp chun a chur in iúl gur comhad ceanntásca C++ comhad. Níl sé riachtanach an síneadh sonrach seo a úsáid le haghaidh comhad ceanntásca, agus is féidir go dtiocfaidh tú trasna ar chomhaid ceanntásca le .h nó síntí eile. Baineann rogha an tsínidh den chuid is mó le gnásanna agus le rogha phearsanta.

Nuair a chuimsíonn comhad foinse C++ comhad ceanntásca ag baint úsáide as `#include`, comhcheanglaíonn an tiomsaitheoir go héifeachtach inneachar an chomhaid header le comhad foinse sula dtiomsaítear é mar aonad. Ligeann sé seo don bhunchomhad rochtain a fháil ar dhearbhuithe agus ar shainmhínithe sa chomhad ceanntásca, ag cur an fhaisnéis is gá ar fáil don tiomsaitheoir chun seiceáil cineáil agus giniúint cód a dhéanamh.

## Cad atá i gcomhad HPP?

Seo roinnt ábhar coitianta a d’fhéadfá a fháil sa chomhad .hpp”:

- **Dearbhuithe feidhme:** Is minic a bhíonn dearbhuithe feidhme san áireamh i gcomhaid cheanntásc nach bhfuil a gcur chun feidhme iarbhír. Soláthraíonn na dearbhuithe seo faisnéis faoi ainm, cineál tuairisceáin agus paraiméadair na feidhme, rud a ligeann do chomhaid chóid foinse eile feidhm a úsáid gan sonraí cur chun feidhme a bheith ar eolas.
- **Dearbhuithe ranga:** Is féidir dearbhuithe ranga a bheith i gcomhaid cheanntásc, lena n-áirítear ainm ranga, athróga ball, feidhmeanna comhaltaí agus sonraíochtaí rochtana. Trí dhearbhú ranga a chur san áireamh i gcomhad ceanntásca, is féidir le comhaid cód foinse eile rudaí den aicme sin a chruthú agus rochtain a fháil ar a chomhaltaí.
- **Dearbhuithe seasmhacha:** Is féidir le comhaid ceanntásca tairisigh a shainiú, amhail athróga domhanda nó luachanna enum a bhfuil sé i gceist iad a roinnt thar chomhaid chóid foinse iolracha. Is féidir teacht ar na tairisigh seo trí chomhad ceanntásca a áireamh i gcomhaid fhoinse eile, rud a ligeann dóibh na tairisigh shainithe a úsáid.
- **Sainmhínithe cineáil:** Féadfaidh sainmhínithe cineáil a bheith i gcomhaid cheanntásc ag baint úsáide as eochairfhocal typedef nó ailiasanna cineáil ag baint úsáide as eochairfhocal ag baint úsáide as. Cruthaíonn na sainmhínithe seo ainmneacha nua do chineálacha atá ann cheana féin, rud a fhágann go bhfuil an cód níos inléite agus inchothaithe.
- **Sainmhínithe ar fheidhm inlíne:** I gcásanna áirithe, féadfaidh sainmhínithe ar fheidhm inlíne a bheith i gcomhaid cheanntásc. Is feidhmeanna beaga iad feidhmeanna inlíne a leathnaítear ar shuíomh glaonna seachas a bheith ar a dtugtar mar fheidhm ar leithligh. Trí shainmhíniú ar fheidhm inlíne a chur san áireamh sa chomhad ceanntásca, is féidir leis an tiomsaitheoir glaoch feidhm a athsholáthar go díreach le comhlacht feidhme, rud a d'fhéadfadh feabhas a chur ar fheidhmíocht.

## Sampla Comhad HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Cad é formáid an chomhaid HPP?

Is comhad gnáth-théacs é HPP ach leanann sé rialacha ginearálta agus comhréir na teanga ríomhchlárúcháin C++. Seo miondealú ar fhormáid ghinearálta agus ar struchtúr an chomhaid .hpp:

- **Gardaí ceanntásc:** De ghnáth, tosaíonn comhad .hpp le gardaí ceanntásc chun cosc a chur ar ilchuimsiú an chomhaid chéanna. Baintear é seo amach trí úsáid a bhaint as treoracha réamhphróiseálaí mar `#ifndef`, `#define` agus `#endif`. Cinntíonn an garda ceanntásc nach gcuirtear inneachar an chomhaid san áireamh ach uair amháin le linn an phróisis tiomsaithe.
- **Cuir san áireamh ráitis:** Tar éis gardaí ceanntásc, is féidir leat comhaid ceanntásc riachtanacha eile a chur san áireamh ag baint úsáide as treoir `#include`. D’fhéadfadh go n-áireofaí orthu seo ceanntásca caighdeánacha leabharlainne nó ceanntásca saincheaptha eile a éilíonn do chód.
- **Dearbhuithe agus Sainmhínithe:** Is é príomhábhar an chomhaid .hpp na dearbhuithe agus, i gcásanna áirithe, sainmhínithe ar aicmí, feidhmeanna, tairisigh, ailiasanna cineáil agus gnéithe eile. Mar shampla, is féidir leat ranganna a dhearbhú ag baint úsáide as eochairfhocal `rang`, feidhmeanna ag baint úsáide as a gcineál tuairisceáin, a n-ainm, agus a liosta paraiméadar, agus tairisigh ag baint úsáide as eochairfhocal `const` agus a gcineál agus a n-ainm ina dhiaidh sin.
- **Sainmhínithe ar Fheidhm Inlíne:** I gcásanna áirithe, féadfaidh tú sainmhínithe ar fheidhm inlíne a chur san áireamh go díreach i gcomhad .hpp. Sainmhínítear feidhmeanna inlíne laistigh de chorp an ranga de ghnáth, rud a chiallaíonn go bhfuil sainmhíniú na feidhme san áireamh taobh lena dhearbhú. Is féidir é seo a dhéanamh trí shainmhíniú feidhme a réamhshocrú le heochairfhocal `inlíne`.
- **Dearbhuithe Ainmspáis:** Má tá spásanna ainmneacha á n-úsáid agat i do chód, is féidir leat iad a dhearbhú laistigh de chomhad .hpp. Déantar é seo trí úsáid a bhaint as eochairfhocal `namespace` agus an t-ainm spásainm ina dhiaidh sin agus an cód ábhartha laistigh den bhloc ainmspáis faoi iamh.

## Tagairtí
* [Comhaid header (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


