---
cssclasses: catalog
date_created: 2025-12-01
publish: true
tags: []   
author: Ueberphilosophy
---
```dataviewjs
dv.executeJs(await dv.io.load("Materialien/breadcrumbs.js"));
```
# Gesamtkatolog Lernmaterialien
Die [Systematik](https://biblio.media.h-da.de/IuD/bibdk1.htm) folgt der DDC, sie verwendet die [[DDCKlassen]] der  [Deutschen Nationalbibliothek](https://www.dnb.de/DE/Professionell/DDC-Deutsch/DDCUebersichten/ddcUebersichten.html)

In der Webversion kann man die Kapitel mit den Unterkatalogen nicht zuklappen. Über die Kapitelüberschrift mit dem Dreieck davor auf der rechten Seitenleisten kann man direkt zum gewünschten Kapitel springen.

## Alle Einträge, sortiert nach DDC
```dataviewjs
await dv.executeJs(await dv.io.load("Materialien/catalog.js"));
```

## Einträge nach Unterverzeichnis
### Geschichte
```dataviewjs
const pages = dv.pages('"Materialien/Geschichte/-Geschichte"');
pages.forEach(i => {dv.el("p","![[" + i.file.link.path + "]]")})
```

### Literatur
```dataviewjs
const pages = dv.pages('"Materialien/Literatur/-Literatur"');
pages.forEach(i => {dv.el("p","![[" + i.file.link.path + "]]")})
```

### Philosophie
```dataviewjs
const pages = dv.pages('"Materialien/Philosophie/-Philosophie"');
pages.forEach(i => {dv.el("p","![[" + i.file.link.path + "]]")})
```

### Wissenschaft
```dataviewjs
const pages = dv.pages('"Materialien/Wissenschaft/-Wissenschaft"');
pages.forEach(i => {dv.el("p","![[" + i.file.link.path + "]]")})
```

### Die fehlenden
```dataviewjs
/* Embedded alle Kataloge der nächsten Tiefe
*/
const eval_foldername = `"${dv.current().file.folder}"`;
const foldername = dv.current().file.folder;

function depth(path) {
    return path.split("/").length;
}
const tiefe = depth(foldername)+1;

const pages = dv
    .pages(eval_foldername)
    .where(p => 
      (p.file.name.substring(0,1) == "-") &&
      (p.file.name != "-Geschichte") &&
      (p.file.name != "-Literatur") &&
      (p.file.name != "-Philosophie") &&
      (p.file.name != "-Wissenschaft") &&
      (depth(p.file.folder)==tiefe) 
     )
    ;
pages.forEach(i => {dv.el("p","![[" + i.file.link.path + "]]")})
```