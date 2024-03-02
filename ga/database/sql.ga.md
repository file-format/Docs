{
  "date": "2020-11-11",
  "keywords": [
"SQL",
"síneadh",
"comhad",
"formáid comhaid",
"Cineál Comhaid Bunachar Sonraí",
"Formáid Comhaid Bunachar Sonraí",
"Comhaid Bunachar Sonraí"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid SQL agus APIs ar féidir leo comhaid SQL a chruthú agus a oscailt.",
  "title": "Formáid Chomhaid SQL - Comhad Sonraí Teanga Iarratas Struchtúrtha",
  "linktitle": "SQL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-sq-gal"
}
},
  "lastmod": "2020-11-11"
}

## Cad is comhad SQL ann?

Comhad le síneadh .sql is ea comhad Teanga Iarratas Struchtúrtha (SQL) ina bhfuil cód chun oibriú le bunachair shonraí choibhneasta. Úsáidtear é chun ráitis SQL a scríobh le haghaidh oibríochtaí CRUD (Cruthaigh, Léigh, Nuashonraigh, agus Scrios) ar bhunachair shonraí. Tá comhaid SQL coitianta agus iad ag obair le deasc chomh maith le bunachair shonraí gréasán-bhunaithe. Tá roinnt roghanna eile ann seachas SQL, mar shampla Java Persistence Query Language (JPQL), LINQ, HTSQL, 4D QL, agus go leor eile. Is féidir le heagarthóirí fiosrúcháin Microsoft SQL Server, MySQL agus eagarthóirí gnáth-théacs eile ar nós Notepad ar Windows OS comhaid SQL a oscailt.

## Stair Ghearr

* Arna fhorbairt agus tugtha isteach ag Donal D. Chamberlin agus Raymond F. Boyce ag IBM go luath sna 1970idí

* Úsáidtear é chun sonraí a stóráil agus a aisghabháil ó bhunchóras bainistíochta bunachar sonraí garghaolta IBM, Córas R

* Cuireadh tús le húsáid i mbonn táirgí tráchtála don fhréamhshamhail Córas R lena n-áirítear System/38, SQL/DS, agus DB2, a bhí ar fáil ar bhonn tráchtála i 1979, 1981, agus 1983, faoi seach.

* Glacadh go hoifigiúil ag grúpaí caighdeánacha ANSI agus ISO mar “Database Language SQL” caighdeánach do chórais bhainistíochta bunachar sonraí coibhneasta (RDBMS) faoi 1986


## Formáid Comhad SQL

Tá comhaid SQL i bhformáid gnáth-théacs agus féadann roinnt gnéithe teanga a bheith iontu. Is féidir ráitis iolracha a chur le comhad SQL amháin más féidir iad a chur i gcrích gan brath ar a chéile. Is féidir le heagarthóirí fiosrúcháin na horduithe SQL seo a fhorghníomhú chun oibríochtaí CRUD a dhéanamh.

### Eilimintí teanga SQL

Tá gnéithe teanga SQL mar atá liostaithe thíos.

|Eilimint|Cur Síos|
---|---|
|Clásail| Comhpháirteanna de ráitis agus de cheisteanna. ||
|Sloinn| Is féidir leis luachanna scálacha, nó táblaí ina bhfuil colúin agus sraitheanna de shonraí a tháirgeadh|
|Predicate| Sonraigh coinníollacha ar féidir iad a mheas go dtí an loighic trí luach SQL (3VL) (fíor/bréagach/anaithnid) nó luachanna fírinne Boole agus úsáidtear iad chun teorainn a chur le héifeachtaí ráiteas agus ceisteanna, nó chun sreabhadh cláir a athrú.|
|Fiosruithe| Aisghabh na sonraí bunaithe ar chritéir shonracha. Is gné thábhachtach é seo de SQL.|
|Ráitis| D’fhéadfadh éifeacht leanúnach a bheith aige ar scéimeanna agus ar shonraí, nó féadfaidh sé idirbhearta, sreabhadh clár, naisc, seisiúin nó diagnóisic a rialú.

### Sampla SQL
Cruthaíonn an ráiteas SQL seo a leanas tábla darb ainm **SONRAÍ**, agus orduithe breise `INSERT` ina dhiaidh chun taifid a chur isteach sa tábla seo.
```
CREATE TABLE DATA
(ID INTEGER REFERENCES STATION(ID),
MONTH INTEGER CHECK (MONTH BETWEEN 1 AND 12),
TEMP_F REAL CHECK (TEMP_F BETWEEN -80 AND 150),
RAIN_I REAL CHECK (RAIN_I BETWEEN 0 AND 100),
PRIMARY KEY (ID, MONTH));
```
```
INSERT INTO STATS VALUES (23, 1, 57.4, 0.31);
INSERT INTO STATS VALUES (21, 7, 91.7, 5.15);
INSERT INTO STATS VALUES (45, 1, 27.3, 0.18);
INSERT INTO STATS VALUES (65, 7, 74.8, 2.11);
INSERT INTO STATS VALUES (78, 1, 6.7, 2.10);
INSERT INTO STATS VALUES (88, 7, 65.8, 4.52);
```

## Tagairtí ##

* [SQL le Vicipéid](https://ga.wikipedia.org/wiki/SQL)

* [Comhréir SQL](https://ga.wikipedia.org/wiki/SQL_syntax)


