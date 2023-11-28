{
"data":"2023-10-11",
   "keywords":[
"ml",
"file mtl",
"file libreria modello materiale mtl obj",
"come aprire un file mtl",
"file",
"estensione file MTL",
"estensione",
"file"
],
   "author":{
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato file MTL - File libreria modelli materiali OBJ",
   "description":"Informazioni sul formato file della libreria di modelli di materiali MTL OBJ e sulle API in grado di creare e aprire file MTL.",
"linktitle": "MTL",
   "menu":{
      "docs":{
         "identifier":"3d-mtl",
"parent" : "3d"
}
},
"lastmod":"2023-10-11"
}

## Cos'è un file MTL?

Il file MTL, abbreviazione di **Material Template Library**, è un formato di file complementare utilizzato nella grafica e nella modellazione computerizzata 3D. È spesso associato al **formato file Wavefront OBJ**, che è un formato comune per l'archiviazione di modelli 3D e dei materiali e delle texture associati.

## Libreria di modelli di materiali

Ecco informazioni importanti sui file MTL:

1. **Definizioni dei materiali**: il file ".mtl" contiene le definizioni dei materiali applicati agli oggetti 3D nel file OBJ corrispondente. Ciascuna definizione di materiale specifica varie proprietà, come colore, lucentezza, trasparenza e mappe di texture.
    





2. **Formato basato su testo**: i file ".mtl" sono in genere file di testo semplice, il che significa che possono essere facilmente modificati con un editor di testo. Ogni definizione di materiale è costituita da una serie di istruzioni e queste istruzioni definiscono gli attributi del materiale.
    





3. **Mappatura texture**: una delle funzioni essenziali di un file ".mtl" è definire come le texture (file immagine) vengono mappate sulle superfici del modello 3D. Specifica il percorso del file di texture e come dovrebbe essere avvolto o applicato al modello.
    





4. **Esempio di istruzioni MTL**: ecco alcune istruzioni di esempio che potresti trovare in un file ".mtl":
    





- "newmtl MaterialName": definisce il nuovo materiale con il nome "MaterialName".
- `Ka rgb`: colore ambientale del materiale, specificato in valori RGB.
- `Kd rgb`: colore diffuso del materiale, specificato in valori RGB.
- `Ks rgb`: Colore speculare del materiale, specificato in valori RGB.
- `Valore Ns`: Lucentezza o esponente speculare del materiale.
- `map_Kd texturefile.jpg`: specifica la mappa texture diffusa per il materiale.
5. **Materiali multipli**: un file OBJ può fare riferimento a più materiali e ciascun materiale è definito nel file ".mtl". Ciò consente modelli 3D complessi con materiali diversi applicati a parti diverse.
    





6. **Compatibilità**: i file ".mtl" sono ampiamente supportati dai software di modellazione 3D e dai motori di rendering, rendendo possibile il trasferimento dei modelli 3D e dei relativi materiali tra diverse applicazioni software.

## Come aprire un file MTL?

I file MTL sono file basati su testo, quindi possono essere aperti con qualsiasi editor di testo incluso

- Blocco note (Windows)
- Blocco note++ (Windows)
- Codice di Visual Studio
- Testo sublime
- Atomo
- Modifica testo (macOS)

I programmi che aprono o fanno riferimento a file MTL includono

- Adobe Photoshop 2023
-Autodesk Maya 2023
- MeshLab
- Ghepardo 3D

**Sottotipo:** File di immagini 3D

## Riferimenti
* [File Wavefront .obj](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

