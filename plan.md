---
cssclasses: note
date_created: 2025-11-30
publish: false
tags: []
author: Ueberphilosophy
---

# Plan
 - [ ] [[Einfuehrung_theoretische_Philosophie_2013_UniHannover_Hoyningen| @Einfuehrung theoretische Philosophie 2013 UniHannover Hoyningen]]
 - [ ] [[-@History_of_Philosophy_without_any_gaps_Adamson| -@History of Philosophy without any gaps Adamson]] Presocratic Philosophy
 - [ ] [[@Stationen_Paradigmen_antike_Philosophie_2017_LMUMuenchen_Buchheim| @Stationen Paradigmen antike Philosophie 2017 LMUMuenchen Buchheim]]
 - [ ] [[Homer Quellen#Illias|Illias]] Librivox Gesang 3
 - [ ] [[@Enuma Elisch|Enuma Elisch]] 28:28 Ende Tafel 2
 - [ ] [[@Grundkurs_alte_Geschichte_UniOldenburg| @Grundkurs alte Geschichte UniOldenburg]] Anfang und die Griechen
 - [ ] [[@Graeber, Wengrow - Anfänge]]
 - [ ] [[@Schadewaldt - Die Anfänge der Philosophie bei den Griechen]]
 - [ ] [[@Nietzsche - Jenseits von Gut und Böse]]
 - [ ] [[@Deleuze - Qu_est-ce que la philosophie]]
 - [ ] [[@Parmenides - Lehrgedicht]]

## technische Entwicklung
- [ ] Plugin
  - [ ] Defaults anzeigen
  - [ ] Einige Werte in Setting speichern (Welche Skriptdatei z.B.)
  - [ ] Formatieren mit css
    - [ ] Breiter
    - [ ] Ok Cancel Knopf
  - [ ] Typen berücksichtigen
  - [ ] Werte editieren lassen
  - [ ] Neue Werte hinzufügen
  - [ ] Neue Typen hinzufügen
  - [ ] Werte/Typen/Defaults löschen
  - [ ] Speichern
- [ ] Nix
## Heute bearbeitete @ Dateien
```dataview
TABLE   regexreplace(file.folder, ".*\\/([^\\/]+)$", "$1")  AS folder
WHERE file.mday = date(today)
AND startswith(file.name, "@")
```
## tote interne Links
%%
```dataviewjs
let r = Object.entries(dv.app.metadataCache.unresolvedLinks) .filter(([k,v])=>Object.keys(v).length) .flatMap(([k,v]) => Object.keys(v).map(x=>dv.fileLink(x)))  
dv.list([...new Set(r)])  
```
%%

```dataviewjs
let result = {};
function process(referingFile, unresolvedLinks) {
    Object.keys(unresolvedLinks).forEach(function (link) {
        link = dv.fileLink(link);
        if (!result[link]) result[link] = [];
        result[link].push(dv.fileLink(referingFile));
    });
}

// Filter for files in a specific directory (e.g., starting with "10 Example Data/dailys")
Object.entries(dv.app.metadataCache.unresolvedLinks)
    .filter(([referingFile]) => {
        return !referingFile.startsWith("allhelperfiles/allvorlagen");
    })
    .forEach(([referingFile, unresolvedLink]) => process(referingFile, unresolvedLink));

// Display the results in a table
dv.table(
    ["Non existing notes", "Linked from"],
    Object.entries(result).map(([unresolvedLink, referingFiles]) => [
        unresolvedLink,
        referingFiles.join(" • ")
    ])
);   
```