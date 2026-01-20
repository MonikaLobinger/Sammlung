---
cssclasses: note
date_created: 2026-01-11
publish: true
tags: []
author: Ueberphilosophy
---
# show_export
## Public, Private, Export
### Exportieren
Aus Obsidian heraus exportieren: von Privat (Export ist ein Sondermodus von Privat) nach Privat. Denn: im privaten Modus ist alles da. Vom Export zu Github wird nur Public exportiert. 
- In Projekte/Schule: Mit ==.prepareforexport== Obsidian in Export Modus schalten. 
- `.prepareforexport` auf jeden Fall aufrufen, auch wenn schon im Export Modus
- `.prepareforexport` nach jedem Aufruf von `git` erneut aufrufen ^[Der Befehl `git` ist durch ein Script überschrieben, das die Leerdateien, die für den Export angelegt wurden, löscht. Dies bei jedem Aufruf.] 
- in schoolout ==.makepriv== aufrufen oder `rm -rf *` ^[Nicht die versteckten Dateien löschen, meine Scripts sind versteckt und `git` sowieso]
- Obsidian `Einstellungen Allgemein Sprache` muss Deutsch sein.
- Aus Obsidian exportieren, Obsidian dabei im Vordergrund lassen ^[Wenn man dabei die Seitenleiste rechts ausblendet, muss weniger gerendert werden]. Falls schoolout gelöscht wurde, mit gelöschtem Cache exportieren. 
- in schoolout .domakepub aufrufen, das ruft u. a. `.adapt_html "domakepub"` auf, das man im Privaten Modus direkt aufrufen kann: `adapt_html "makepriv"`.
- Das testet auch den output, wenn der nicht stimmt, unvollständige Dateien touchen und neu exportieren
- in schoolout git add, git commit, git push
- in schoolout .makepriv aufrufen
- In Projekte/Schule: Mit .makepriv den Exportmodus aufheben oder nur mit einem Aufruf von ggit oder direkt mit .erstelleleeremitschriften "wegdamit" die Leermitschriften löschen
### Einchecken
tl;tr In den Modus `Public` oder `Export` schalten; ==ggit== Befehle aufrufen


Die Scriptdatei `.makepriv` wechselt zum privaten Repository und `.domakepub` wechselt zum öffentlichen Repository. `.prepareforexport` sollte keinen Wechsel vollziehen. Damit wäre immer sichergestellt, dass man mit dem richtigen Repository verbunden ist. Ausserdem kann man das private Repository nur im Modus `Export` einchecken.

Der `git` Befehl wäre durch ein lokales Script `git` überschrieben, das sicherstellt, dass man sich im Modus `Public` oder `Export` befindet und im nochmal sicherstellt, dass man sich wirklich mit dem richtigen Repository verbunden ist. Ausserdem löscht es die Leerdateien, die nur dafür erstellt wurden, daß der Export Links auf Werkstatt Dateien generiert, die es im Privaten Repository nicht gibt, aber im öffentlichen.

Leider kann vims Plugin git-gutter nicht mit diesem Git Script. Deswegen heißt es nun `ggit` und kann per Hand aufgerufen werden. Einmal muß es vor dem Einchecken aufgerufen werden, denn es löscht die Leermitschriften.

## -footnotes
