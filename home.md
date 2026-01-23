---
cssclasses: note
date_created: 2025-11-24
publish: true
author: Ueberphilosophy
---

# Nonmatrikulation
Sammlung von Vorlesungen und frei zugänglichen Primärquellen
## Inhaltsverzeichnis Hauptbereiche
 &nbsp;&nbsp;&nbsp;&nbsp;[[home#Studieren von zu Hause aus|Allgemein]]  
 &nbsp;&nbsp;&nbsp;&nbsp;[[home#Bedienung der Site|Bedienung Netz]]  
 &nbsp;&nbsp;&nbsp;&nbsp;[[home#Inhalt|Inhalt der Site/des Vaults]]  
 &nbsp;&nbsp;&nbsp;&nbsp;[[home#Erschliessung|Erschliessung]]  
 &nbsp;&nbsp;&nbsp;&nbsp;[[home#Benutzung des Obsidian Vaults|Bedienung Obsidian]]  
 &nbsp;&nbsp;&nbsp;&nbsp;[[home#Technisches über die Quellen und deren Export|Technisches]]
## Allgemein: Studieren von zu Hause aus
Sammlung von Links zu __Materialien__ (Vorlesungen als Audios oder Videos) __[[-Materialien|als Katalog]]__/__[[Materialien|als Verzeichnis]]__  und frei zugänglichen __Quelltexten__ (Primärquellen) __[[Materialien/timeline|als  Zeitleiste]]__/__[[Autoren|als Verzeichnis]]__. 

Diese befindet sich als kaum kommentierte Linksammlung im Ordner `Materialen`. Der Ordner `Werkstatt` kann in der lokalen Version (dem Obsidian Vault[^1]) für jeweils eigene Notizen verwendet werden. Im Ordner `Zusaetze` sind  zusätliche Seiten, die die Sammlung ergänzen. Die selbst erstellen Definitionen im Ordner `Zusaetze/Definitionen` sind grob, auf den Themenseiten im Ordner `Zusaetze/Themen` finden sich Links zu bestimmten Themen.

Die Sammlung ist im Netz als statische Site veröffentlicht. Die [Quellen](https://github.com/MonikaLobinger/Nonmatrikulation) sind ein [Obsidian](https://obsidian.md/) Notebook - damit kann man sich den Vault[^1] als lokale Version einrichten.
## Bedienung der Site
 - Klick vor (links neben) Überschriften klappt den Inhalt ein, nochmaliger Klick wieder auf; das zugehörige Symbol wird beim Drüberfahren mit der Maus sichtbar. 
 - Ganz oben links und rechts kann man die Seitenleisten ein- und ausblenden
 - Auf der rechten Seitenleiste oben kann man dunkle oder helle Anzeige einstellen.
 - Im Suchfeld auf der linken Seitenleiste oben durchsucht man alle Seiten. Nach Tags sucht man mit vorrangestelltem Doppelkreuz: `#tagname`. 
 - Beim  Klick mit der Maus öffnen alle Links, auch externe,  im selben Fenster. `Ctrl` (deutsch: `Strg`)-Klick öffnet in einem neuen Tab.
 - Links auf Überschriften funktionieren nur innerhalb der aktuellen Seite ^[Das ist wohl dem Plugin  [Webpage HTML Export](https://github.com/KosmosisDire/obsidian-webpage-export); doch es exportiert die Seitenleisten mit der Ordnerstruktur und der Dateistruktur ohne Anpassung ohne Probleme, darum behalte ich es bei, hoffend, dass es verbessert wird.], entsprechend zeigen die Hovers auf Überschriften anderer Seiten den Seitenanfang an.    Die exportierte Sammlung verwendet in den Katalogen Links auf Überschriften der DDC Klassen und von den Autorenseiten Links auf Überschriften in die Zeitleiste. Für beide wird der Fehler in den Html-Dateien durch ein Script korrigiert. ^[In der Verlinkung wird an die Überschrift "_0" angehängt, so dass sie funktioniert. Da die Sammlung auch direkt in Obsidian verwendet wird und dort "_0" nicht zum Link gehört, wird das nicht in den Quellen angepasst]
 - Links auf Anker funktionieren in der exportierten Sammlung grundsätzlich nicht. ^[Auch das wohl dem Plugin [Webpage HTML Export](https://github.com/KosmosisDire/obsidian-webpage-export) geschuldet, denn in Obsidian selbst funktioniert das.]. z.B. [[home#^textformate|Verlinkung zu Anker Textformate auf dieser Seite.]]
 - Entsprechend würde die Verlinkung von Fußnoten nicht funktionieren, da diese über Anker realisiert sind. Für sie wird die Verlinkung allerdings in den Html-Dateien durch ein Script korrigiert. Ein Hover Effekt wird dadurch nicht hergestellt.
 - Das Kopieren von Code Blöcken mit dem `Kopieren`-Icon funktioniert nicht.
%% Den Dateibaum anpassen
site-lib/html/file-tree-content.html

```
:%s/<div class="tree-item-self is-clickable mod-collapsible nav-folder-title" data-path="Werkstatt"\_.\{-}zzzzzz<\/div><\/a><div class="tree-item-children nav-file-children"><\/div><\/div><\/div><\/div>//
```

Batch `.makepriv` im Verzeichnis `/opt/lampp/htdocs/schoolout` aufrufen
```
#!/usr/bin/env bash
cp site-lib/html/file-tree-content.html site-lib/html/file-tree-content.sv
sed -i 's/<div class="tree-item-self is-clickable mod-collapsible nav-folder-title" data-path="Werkstatt".*zzzzzz<\/div><\/a><div class="tree-item-children nav-file-children"><\/div><\/div><\/div><\/div>//' site-lib/html/file-tree-content.html
```
`.domakepub` stellt die öffentliche Version wieder her
%%

%% 
Der gesamte Ablauf des Exports steht in [[2025-12-14#Wie es läuft]]
%%

## Inhalt
Die Netzversion/die lokale Version, anders ausgedrückt die Site/der Vault  besteht aus einem öffentlichen und einem privaten Bereich. Der private Bereich ist im Ordner "Werkstatt". Er ist für eigene Notizen jeglicher Art gedacht und macht in der Netzversion keinen Sinn.

Das Kernstück des öffentliche Bereichs ist der Ordner [[Materialien]]. Es wird unterschieden zwischen Lernmaterialen, hauptsächlich Videos und Audios,  und Quellen. Lernmaterialen sind über ein Thema, Quellen sind  frei zugängliche Originaltexte. Für Lernmaterialien gibt es einen  [[-Materialien|Katalog]] nach Bereichen. Quellen sind nach Autoren unterschieden, sie sind über die [[Materialien/timeline|Zeitleiste]]  zu finden. Der Katalog wird automatisch erstellt, die timeline manuell. Beide Bereiche sind auch über das [[Materialien|Inhaltsverzeichnis]] zugänglich. Über die Seitenleiste links kann man alle Seiten finden. Die Dateinamen der Kataloge beginnen mit einem Bindestrich, die Dateinamen der Inhaltsverzeichnisse heissen wie die Verzeichnisse, die sie auflisten.
- Grobe [[Materialien/timeline|Zeitleiste]]  mit Links zu Quellenseiten (verknüpft über den Autorennamen)
- [[-Materialien|Katalog]] mit Links zu thematischen Sammlungen von  Links zu Lernmaterialen
## Erschliessung
Ein physikalisches Buch steht genau einmal an einem bestimmten Platz. In Computern ist das anders. Man könnte nun meinen, wenigstens eine Datei müsse genau einmal irgendwo liegen, doch das stimmt nicht. Die selbe Datei könnte zweimal auf einem Speichermedium liegen. Änderte man sie an einem Ort, wäre sie auch am anderen verändert, da es die selbe Datei ist. So könnte eine Datei die eine Veranstaltung "evolutionäre Erkenntnistheorie" beschreibt, einmal im Ordner Philosophie und einmal im Ordner Biologie liegen. Dieser Ansatz wurde in [Nonmatrikulation](https://github.com/MonikaLobinger/Nonmatrikulation) nicht gewählt. Bei der Ablage der Dateien wird wie bei physikalischen Objekten verfahren. Jede Datei, auch eine Datei mit einer Veranstaltungsbeschreibung liegt immer genau einmal in einem bestimmten Ordner. So kann man sich sicher sein, wenn man eine Datei über Ordnersuche findet, dass man die selbe Datei nicht in einem anderen Ordner findet (und so vielleicht ohne es zu merken die selbe Veranstaltung zweimal auf seine "WillIchHören" Liste schreibt).
### Inhaltsverzeichnisse
Veranstaltungen liegen in Ordnern [[Materialien]]. Bis auf [[Autoren]] (und [[Autoren-Sekundaer]]) enthalten alle Unterordner in [[Materialien]] Veranstaltungen oder Unterordner mit Veranstaltungen. Inhaltsverzeichnisse in [[Materialien]] heißen wie der Ordner. Ein [[Inhaltsverzeichnis|Hauptinhaltsverzeichnis]] liegt parallel zu dieser Datei.
### Kataloge
Die Deutsche Nationalbibliothek wartet die [Dewey-Dezimalklassifikation auf deutsch](https://www.dnb.de/DE/Professionell/DDC-Deutsch/ddc-deutsch_node.html), kurz DDC. Jeder Veranstaltung wird ein Attribut `DDC` mit einer dreistelligen DDC Nummer gegeben. Entscheidet man sich die Veranstaltung "evolutionäre Erkenntnistheorie" im Bereich Philosophie abzulegen, bekommt sie die DDC Nummer 121, legte man sie in Biologie ab, bekäme sie die DDC Nummer 576. 

Die DDC Nummern werden in Katalogen angezeigt. Die Kataloge sind nach DDC Nummern sortiert. Im [[-Materialien|Hauptkatalog]] sind alle Veranstaltungen im Verzeichnis Materialien aufgelistet, in Unterkatalogen, z.B. [[-Sprachphilosophie|Sprachphilosophie]] entsprechend nur die Veranstaltungen des entsprechenden Verzeichnisses.
### Vernetzung
Nichtlineare Verbindungen in Dateien/Notizen können auf drei Arten gefunden und/oder erstellt werden.
#### Tags
Ein Wort, dem ein Doppelkreuz vorangestellt ist, wird zu #tag. Klickt man darauf, werden im rechten Seitenbereich alle Dateien angezeigt, die dieses #Tag enthalten.
#### Links
Notizen können untereinander verlinkt sein. In beiden Versionen kann man wie üblich auf diese Links klicken. In der Netzversion werden die Rückverweise (Backlinks) unten auf der Seite angezeigt. In der lokalen Version kann man verschiedene Rückverweis Bereiche anzeigen. 
#### Suche nach einem Wort
Nach jeder bestimmten Buchstabenfolge kann über alle Dateien in der Netzversion in der linken Seitenleiste gesucht werden; in der lokalen Version ist greift man auf diese Suche über den Befehl `Suchen: in allen Dateien suchen` zu, die Ergebnisse werden dann auch links in der Seitenleiste angezeigt. 

## Benutzung des Obsidian Vaults
Wird diese Seite in Obsidian gelesen, wurde [der Obsidian Vault](https://github.com/MonikaLobinger/Nonmatrikulation)^[Ein Notizbuch  heißt in Obsidian Vault] heruntergeladen. Dieser Vault enthält keine Plugins. Im Abschnitt [[home#Einstellungen und Plugins in Obsidian|Einstellungen und Plugins für Obsidian]] ist beschrieben, wie dieser Vault bei der Erstellung der Quellen eingerichtet war. Das braucht man nicht alles, um ihn zu benutzen. Auch wurde dort die Anzeigesprache Englisch verwendet. Hier wird für ein auf Deutsch eingestelltes Obsidian beschrieben, wie man den Vault einrichtet, um ihn fürs Selbststudium gut nutzen zu können.

### Einstellungen
Mit der Tastenkombination `Strg-,`^[Steuerung Komma] öffnet man den Dialog Einstellungen. Dieser hat links sieben Einträge im Abschnitt "Optionen" und noch einige im Abschnitt "Obsidian-Erweiterungen".   
#### Allgemein
Im Eintrag Allgemein stellt man die Sprache auf "Deutsch" ein.
#### Editor
Im Eintrag Editor schaltet man "Strenge Zeilenumbrüche" ein und "Eigenschaften im Dokument" auf "Nicht sichtbar". Besonders für Obsidian Neulinge würde ich entgegen gängiger Meinung empfehlen, den dritten Eintrag "Standardmodus zum Bearbeiten" auf "Quellcode-Ansicht" zu stellen. Weitere Einstellungen wählt man nach Belieben. ^Bearbeitungsmodus
#### Dateien & Links
Im Eintrag Dateien & Links schaltet man "Standardordner für neue Notizen auf "Eigenen Ordner unten festlegen". Ebenso schaltet man "Standardordner für neue Anhänge" auf "Eigenen Ordner unten festlegen". Danach erscheint jeweils eine neue Option direkt darunter.

- In "Ordner für neu erstellte Notizen" trägt man "Werkstatt" ein.
- In "Ordnerpfad für Anhänge" trägt man "allhelperfiles/allresources" ein
- "Interne Links automatisch aktualisieren" schaltet man ein

Weitere Einstellungen wählt man nach Belieben.
#### Darstellung
Im Eintrag Darstellung würde ich empfehlen "Zeige Titel in Notiz" auszuschalten und "Zeige Tab-Titelleiste" eingeschaltet zu lassen.  Eines von beiden muß auf jeden Fall ein sein. Weitere Einstellungen wählt man nach Belieben.

Ganz unten in "Darstellung" gibt es einen gibt es Abschnitt "CSS-Bausteine". Dort sind drei Einträge: "adapt", "obsidian-source-view" und "timeline". Dies enthalten die von [Nonmatrikulation](https://github.com/MonikaLobinger/Nonmatrikulation) mitgelieferten Css Einstellungen. Damit es so aussieht wie im Netz sollten "adapt" und "timeline" eingeschaltet werden. Nutzt man zum Editieren die [[home#^Bearbeitungsmodus|Quellcode Ansicht]] sollte man auch "obsidian-source-view" wählen. Dies zeigt beim Editieren alle Zeilen gleich hoch an, die Überschriften werden dafür mit hellgelbem Hintergrund hervorgehoben. Weiterhin werden die Links direkt als Buchstabenfolgen (und nicht als Links) dargestellt; für einen Vault mit vielen Links eine nützliche Einstellung beim Editieren.
#### Tastenkürzel
Im Eintrag Tastenkürzel stellt man die einem selbst angenehmen Tastenkürzel ein. Oder man kopiert direkt eine Datei "hotkeys.json" in das Verzeichnis ".obsidian". Dies würde bereits definierte Tastenkürzel entfernen. [Nonmatrikulation](https://github.com/MonikaLobinger/Nonmatrikulation) liefert eine Datei "hotkeys.json" mit. Diese kopiert man ins ".obsidian" Verzeichnis. In einer Shell in Linux geht das so: 
```
# In einer Bash Shell sicher stellen, dass man sich in der Wurzel des Vaults Nonmatrikulation befindet
pwd
# Ebenso sicher stellen, dass keine Datei .obsidian/hotkeys.json existiert
ls .obsidian/hotkeys.json
# Mitgelierte Tastenkürzel kopieren
cp allhelperfiles/pointobsidian/hotkeys.json .obsidian/
```
Danach kann man z.B. mit `Alt-Pfeilrechts` die rechte Seitenleiste ein- und ausblenden, mit `Alt-Pfeilhoch` rückwärts navigieren oder mit `Strg-d` das aktuelle Datum einfügen.
#### Obsidian-Erweiterungen
Im Eintrag Obsidian-Erweiterungen schaltet man von Obsidian selbst mitgelieferte Erweiterungen nach Belieben ein- oder aus.
#### Externe Erweiterungen
Im Eintrag externe Erweiterungen drückt man auf den Knopf "Community-Erweiterungen aktivieren". Damit hat man externe Plugins ermöglicht. Man drückt auf den Knopf "Durchsuchen" und installiert die im folgenden Kapitel vorgestellten Plugins.

### Man benötigt einige Plugins
Nach der Installation eines externen Plugins gibt es im Einstellungsdialog `Strg-,` links einen dritten Abschnitt "Externe Erweiterungen". Dort kann man die Einstellungen für diese Plugins vornehmen. Einige Plugins haben keine Einstellungen, diese tauchen in diesem Abschnitt nicht auf.
#### Templater
Das Plugin Templater ist vom Entwickler "SilentVoid" und wurde über 3 Millionen mal installiert. Nach der Installation muß man auf den Knopf "Aktivieren" klicken.

In den Einstellungen von Templater Templater einrichten:
- "Template folder location "allhelperfiles/allvorlagen"
- "Automatic jump to cursor" an
- "Trigger Templater on new file creation" an
- "Enable folder templates" an
- Direkt in der Zeile darunter in "Folder" `/` eintragen und in "Template" `allhelperfiles/allvorlagen/foty_Vorlage.md`
- "Script files folder location" `allhelperfiles/allscripts`
#### Dataview
Das Plugin Dataview ist vom Entwickler Michael Brenan und wurde über 3 Millionen mal installiert. Nach der Installation muß man auf den Knopf "Aktivieren" klicken.

In den Einstellungen von Dataview Dataview einrichten:
- "Enable Javascript Queries" an
#### Waypoint
Das Plugin Waypoint ist vom Entwickler Idrees Hassan und wurde über 90 Tausend mal installiert.  Nach der Installation muß man auf den Knopf "Aktivieren" klicken.
### Weitere Einrichtung
[Nonmatrikulation](https://github.com/MonikaLobinger/Nonmatrikulation) bietet folgende Features
- [[timeline|eine Zeitleiste]]
- Breadcrumbs oben in jeder [[Apollodoros Quellen|Materialien Datei]]
- [[Materialien/Geschichte/-Geschichte|Veranstaltungskataloge]]
- [[Philosophie|Verzeichnisse]]
- Anzeige aller [[@Einfuehrung_Philosophie_1950_Karl_Jaspers|Mitschriften]] mit einem gelben Rand rechts und links.
- Erstellung von neuen Notizen mit `Strg-n` automatisch im Verzeichnis "Werkstatt"
- Neue Notizen im Verzeichnis Werkstatt sind typisiert, beim Erstellen einer neuen Notiz erscheint eine Auswahlliste.

Wurden die Einstellungen und Erweiterungen wie oben angegeben eingerichtet, funktioniert das alles. Im Abschnitt [[home#Technisches über die Quellen und deren Export|Technisches über die Quellen und deren Export]] werden die verwendeten Techniken genauer beschrieben und weitere Plugins vorgestellt.
## Technisches über die Quellen und deren Export
### Einstellungen und Plugins in Obsidian
- Erstellt mit [Obsidian](https://obsidian.md/), 
- Einstellungen 
  - Editor
    - Default editing mode: Source mode 
    - Strict Line Breaks, 
    - Properties in Document hidden, 
    - Show line numbers, 
    - Kein Auto-pair brackets
    - Kein Auto-Pair Markdown Syntax
    - vim-key bindings, 
  - Files and Links
    - New notes nach: `Werkstatt`
    - Attachments nach `allhelperfiles/allresources`  
  - Appearance
    - Nicht Show Inline Title
    - CSS-Snippets: Lade adapt.css, obsidian-source-view.css, timeline.css
   - Hotkeys
    - Eigene Shortcuts in `.obsidian/hotkeys.json` ^[hardlinked zu `allhelperfiles/pointobsidian/hotkeys.json`, damit es im Vault gesehen werden kann, dies hat keinen Einfluss auf die Funktionalität].
  - Diary 
    - Verzeichnis für Daily Notes `Werkstatt/Diary`. 
  - Templates
    - template folder location  `allhelperfiles/allvorlagen`.  
- Core Plugins aus: Canvas, Graph View, Note Composer, Sync
- Sonst Defaults, 
- exportiert mit dem Plugin [Webpage HTML Export](https://github.com/KosmosisDire/obsidian-webpage-export).
  - Einstellungen Webpage HTML Export
     - Abschnitt Page Features
       - Graph View aus
       - Custom HTML/JS ^[Fügt den Inhalt von banner.html in ein div.parsed-feature-container als erstes div in body ein, nach einem (davon unabhängigen) style element]
         - Source: banner.html
         - Feature Placement: body start
       - Backlinks aus
       - Tags Feature Placement `Start` von `.footer .data-bar` 
       - RSS aus
- Editmode angepasst mit eigener Datei `obsidian-source-view.css`. 
- Export angepasst in eigener Datei  `adapt.css`. 
- dort auch die css Klassen definiert
- Eigenes Script `foty.js` nach `allhelperfiles/allscripts`, ^Script
- Eigenes Template `foty_Vorlage.md` nach `allhelperfiles/allvorlagen`. ^Vorlage
- Eigene vimrc Anpassung `vimrc.js` ^[Hauptsächlich um sich im Insert Mode mit Alt-h, Alt-j, Alt-k, Alt-l bewegen zu können.]
- Plugin [Templater](https://github.com/SilentVoid13/Templater) erstellt neue Notes mit [[home#^Script|Script]] `allhelperfiles/allscripts/foty.js` und [[home#^Vorlage|Vorlage]] `allhelperfiles/allvorlagen/foty_Vorlage.md`
  - Einstellungen Templater
    - Template Folder Location `allhelperfiles/allvorlagen`
    - automatic jump to cursor, 
    - Trigger Templater on new file creation, 
    - Enable folder templates, 
    - folder template `/` `allhelperfiles/allvorlagen/foty_Vorlage.md`, 
    - Script files folder location `allhelperfiles/allscripts`
    - Kein enable file regex template
- Plugin [Dataview](https://blacksmithgu.github.io/obsidian-dataview/)
  - Einstellungen Dataview
    -  Enable Javascript Queries
- Plugin [Shortcuts Extender](https://github.com/ryjjin/Obsidian-shortcuts-extender) ^[Nur wegen des Backticks für Code, insbesondere des dreifachen Backticks für Code Blöcke]
- Plugin [ProZen](https://github.com/cmoskvitin/obsidian-prozen)
- Plugin [Typewriter Mode](https://github.com/davisriedel/obsidian-typewriter-mode)
- Plugin [Waypoint](https://github.com/IdreesInc/Waypoint) ^[zum Erstellen der Inhaltsverzeichnisse]
- Plugin [Foldernotes](https://github.com/LostPaul/obsidian-folder-notes) ^[für die Eingliederung der Verzeichnisseiten in Obsidian]
  - Einstellungen
    - File Explorer
      - Open Folder Notes by only clicking directly on the folder name anwählen
- Plugin [Quickadd](https://github.com/chhoumann/quickadd) ^[um damit beim Start das  selbsterstellte Script vimrc.js zu laden.]
- Plugin [Calendar](https://github.com/liamcain/obsidian-calendar-plugin) inklusive einer [Anpassung](allhelperfiles/pointobsidian/plugins/calendar/main.js), mit der der Befehl `Calendar: Open view` funktioniert.
- Plugin [Chronology](https://github.com/Canna71/obsidian-chronology)
- Plugin [Recent Files](https://github.com/tgrosinger/recent-files-obsidian)
- Für Zeitleiste [Timeline Callout von FirelsGood](https://github.com/r-u-s-h-i-k-e-s-h/Obsidian-CSS-Snippets/blob/Collection/Snippets/Callout%20styling%20-%20Timeline%20callout.md), leicht angepasst, als `timeline.css`. 
- Plugin [Hot-Reload](https://github.com/pjeby/hot-reload#) manuell installiert ^[um einfacher eigenes Plugin vim-fuer-sammlung zu entwickeln]
- eigenes Plugin vim-fuer-sammlung zum Anzeigen des Vim Modes in der Status Bar.
- 
### vim Anpassungen
- Im Edit Mode soll man sich ohne Pfeiltasten bewegen können
- Dass man sich im Edit Mode befindet soll deutlich angezeigt werden

Mit dem zuerst verwendete Plugin [obsidian-vimrc-support](https://github.com/esm7/obsidian-vimrc-support) gab es keine Möglichkeit auf die Pfeiltasten zu mappen. Ausserdem zeigt es den Vim Mode nicht zuverlässig an.

[The Ultimate Guide to Customizing Obsidian Vim Mode via QuickAdd](https://blog.iany.me/2023/04/the-ultimate-guide-to-customizing-obsidian-vim-mode-via-quickadd/) beschreibt, wie man ohne ein Plugin zu erstellen, direkt mittels einer Javascript Datei Vim anpasst, zum Beispiel Mappings erstellt.

Damit als Vorlage erstellt die eigene Datei [[vimrc.js]] einfache Befehle um sich hoch, runter, nach rechts und nach links zu bewegen und weist diese, auch im Insert Mode, den Tastenkombinationen \[Alt-k\], \[Alt-j\], \[Alt-l\] und \[Alt-h\] zu; sie wird mit dem Modul QuickAdd beim Start geladen.

Wie man den Vim Mode in der Statusbar anzeigt, ist im verworfenen Plugin [obsidian-vimrc-support](https://github.com/esm7/obsidian-vimrc-support) implementiert. Dieser Code wurde in das eigene Plugin [vim-fuer-sammlung](https://github.com/MonikaLobinger/vim-fuer-sammlung) übernommen. Die zugewiesene Css Klasse `vim-sammlung-statusbar` wird im snippet `adapt.css`  im Edit Mode deutlich hervorgehoben.

Diese beiden Ansätze könnte man vereinigen. Aber sie wurden von unterschiedlichen Vorlagen mit unterschiedlichen Prinzipien erstellt und ich bin kein Profi für Obsidian Anpassungen. 
### Das verwendete Template foty
[foty](https://github.com/MonikaLobinger/foty) ist ein Template, mit dem es möglich ist, automatisch in verschiedene Verzeichnisse unterschiedliche Notizgerüste einzufügen.

Es ist ein bisschen kompliziert aber mächtig. Vielleicht ist das Script leichter zu verstehen, wenn man sich bewusst macht, dass jedes Templater Script von der Vorlage ausgeht.

#### Das Templater Plugin
Der [Templater](https://github.com/SilentVoid13/Templater) arbeitet mit Templates, Vorlagendateien. Er hat verschiedene Möglichkeiten, sie einzufügen. 

In einem Templater Template kann man Zwischen Klammerausdrücken `<%*` und `%>` jeglichen Javascript Code schreiben, in dem man z.B. eine Stringvariable `strout` füllen kann. Diese kann man dann in einem anderen Block direkt in das Gerüst der neuen Datei schreiben: `<% strout _`. (Dieser Block wird von <% ohne Stern eingeleitet)

Zusätzlich bietet der Templater die Möglichkeit Script Dateien einzubinden. Die von diesen Dateien exportierten Funktionen können von den Templates aufgerufen werden.

Wenn eine Script Datei mit `module.exports = foty` die Funktion `foty` exportiert, kann sie in einer Vorlagendatei aufgerufen werden: `<%* tp.user.foty(tp, app) %>`.

Was zwischen `<%*` und `%>` ausgeführt wird, ist echtes Javascript. Doch es steht nicht in einer Javascript Datei.
#### Folder Templates
Deswegen habe ich die Logik soweit als irgend möglich in ein (ein einziges) Script verlegt und gleichzeitig die Anzahl der benötigten Vorlagen (Templates) auf eins reduziert.
#### foty_Vorlage.md
Diese eine Vorlage ruft die eine exportiert Funktion auf, die Funktion macht die ganze Arbeit und gibt der Vorlage dann die gewonnen Werte. Die Werte können entweder YAML (Frontmatter, was auf Deutsch in den Editor Einstellungen von Obsidian "Eigenschaften im Dokument" heißt) sein oder Textschnipsel, die direkt in die Notiz eingefügt werden. 

foty hat die Konvention, dass alles was vor "____" gesendet wird YAML Eigenschaften sind - diese sind recht einfach zu bearbeiten, sie werden so wie sie kommen in den Eigenschaftenbereich am Anfang der Notiz geschrieben.

Alles was danach kommt kommt direkt in die Notiz. Aber wie? Da müssen die Vorlage und das Script gemeinsame Namen haben, z.B. "pict", "firstline", "prevlink" und es müssen sich beide einig sein, was mit dem jeweiligen Schnipsel gemacht wird.
#### foty.js
Das Script ist solides Handwerk ohne Benutzeroberfläche. 

##### Voraussetzungen
Damit es läuft, muß im Templater
- die Template folder location auf das Verzeichnis von foty_Vorlage.md gesetzt sein
- Trigger Templater on new file creation aktiviert sein
- Enable Folder Templates aktiviert sein
- Und dafür eine einzige Regel: Für alle Dateien (also links die Wurzel `/` angeben) soll foty_Vorlage (rechts angeben) eingefügt werden.
- die Script file folder location auf das Verzeichnis von foty.js gesetzt sein.
##### was foty tut
Vielleicht hat man ein Verzeichnis Garten und eines Bibliothek und möchte in jedes dieser Verzeichnisse ein Tagebuch einfügen. Das allgemeine Tagebuch möchte man auch führen. Dann könnte man die Verzeichnisse /Tagebuch, /Garten/Tagebuch und Bibliothek/Tagebuch anlegen und einen NoteType erstellen, den man z.B. tagebuch nennt und für den der Wert folders ["Tagebuch"] ist. Dann würden alle Notizen in jedem Verzeichnis Tagebuch oder einem Unterverzeichnis davon mit der Variante von foty_Vorlage.md erstellt werden, die man fürs Tagebuch möchte, z.B. "publish: -nein" und als Titel das aktuelle Datum und eine automatische Verlinkung auf den vorigen Eintrag und den morgigen (wenn man erst übermorgen wieder schreibt muss man das per Hand ändern.)

Oder man möchte all seine Notizen in einem Verzeichnis haben, Bücher, Rechnungen, Filmbeschreibungen, damit man die aber visuell unterscheiden kann sollen sie je nach Typ mit einem anderen Kenner anfangen. Man könnte drei NoteTypes erstellen: buch, rechnung, film, derem folders ["Einträge", "vielleicht"] sind. Bücher sollen mit {b} beginnen, filme mit $ und Rechnungen mit - . Man setzt die marker der NoteTypes entsprechend.

Erstellt man dann eine Notiz in einem Verzeichnis "Einträge" oder "vielleicht" wird einem die Auswahl zwischen buch, rechnung, film angeboten. Nach der Auswahl gibt man den Dateinamen name ein und es wird für ein Buch eine Notiz {b}name, für einen Film $name und für eine Rechnung -name erzeugt. Die YAML Einträge und die Notizgerüste werden so erzeugt wie im jeweiligen NoteType angegeben.
##### wie man es bedient
###### Beispiel 1
```
let example_configuration1 = {
  SECTION_NOTETYPES: {
    note: {
      marker: "{w}",
      yaml: {__SPEC: {RENDER: false,}, aliases: aliasOrt, borgia: "Lucrezia", },
      show: {__SPEC: {RENDER: true,}, firstline: "DAS WORT", fugger: true, },
    },
  }
}
```
Ein einziger NoteType "note", der für alle Verzeichnisse gilt. Jede Datei hat vor dem eigentlichen Namen den Kenner {w}. In den YAML Kopf wird aliases: und borgia: geschrieben. aliases hat einen Wert der durch die Funktion aliasOrt bestimmt wird (diese ignoriert den Kenner und macht noch was mit Kommas) und borgia hat den Wert "Lukrezia".

Dem Template wird als firstline "DAS WORT" gegeben. Das Template foty_Vorlage fügt firstline als erste Zeile (nach scriptline) ein, und zwar als Überschrift der Stufe eins. Zwar ist fugger wahr (true), doch das Template macht nur was, wenn auch lastline gesetzt wäre und das ist es nicht.

Hier sieht man, daß das Script und die Vorlage in der Übergabe übereinstimmen müssen. Die Schlüssel "borgia" und "fugger" sind absichtlich schräg gewählt, so dass deutlich wird, dass die Namen egal sind.
###### Beispiel 2
```
let example_configuration2 = {
  SECTION_TRANSLATE: { TITLE_NEW_FILE: "Unbenannt",  },
  SECTION_NOTETYPES: {
    defaults: {
      __SPEC: {REPEAT: true},  
      yaml: {__SPEC: {RENDER: false,},
        publish:          {__SPEC:false, DEFAULT: true, TYPE: "Boolean", },
      },
      show: { __SPEC: {RENDER: true,},
        type:      {__SPEC:false, DEFAULT: cbkNoteType, TYPE: "(String|Function)",},
        firstline: {__SPEC:false, DEFAULT: "First Line", TYPE: "String",},
        lastline: {__SPEC:false, DEFAULT: "##Footnotes", TYPE: "String",},
      },    
    },
    book: { folders: ["book"], },
    test: { folders: ["test"], yaml: { publish: false, }, },
  }
}
```
Für Obsidian, das auf Deutsch läuft, muss unbedingt TITLE_NEW_FILE auf "Unbenannt" gesetzt werden.

Was im Abschnitt "defaults" steht, gilt für jeden Notiztyp. Jede Notiz wird also einen YAML Eintrag publish mit dem Wert true erhalten. Sie kann den Wert allerdings überschreiben, so wie das der NoteType test macht. Jede Notiz wird type, firstline und lastline an die Vorlage senden. type wird von der Callback Funktion cbkNoteType bestimmt, die den Foldertype zurückgibt, hier also entweder book oder test. Aber unsere Vorlage foty_Vorlage macht nichts mit type. Da stimmt was mit der Kommunikation nicht.

Der NoteType book übernimmt die Vorgaben, der notetype test überschreibt publish mit false.
###### Beispiel 3/Folder

```
let schule_configuration = {
    LANGUAGE: "de", // hardcoded:FALLBACK_LANGUAGE "en"
  },
  SECTION_TRANSLATE: {
    TITLE_NEW_FILE:      [ ["en", "Untitled"], ["de", "Unbenannt"] ],
  },
  SECTION_NOTETYPES: {
    __SPEC: {DEFAULT: "note"},
    defaults: {
      __SPEC: {REPEAT: true},
      schoolyaml: {__SPEC: {RENDER: false,},
        cssclasses:  {__SPEC:false, DEFAULT: cbkFmtCC, TYPE: "(Array.<String>|Function)"},
        author:      {__SPEC:false, DEFAULT: "Tulpe Riesengross", TYPE: "String", },
        publish:     {__SPEC:false, DEFAULT: true, TYPE: "Boolean", },
      },
      schoolshow: { __SPEC: {RENDER: true,},
        prevlink:  {__SPEC:false, DEFAULT: "", TYPE: "(String|Function)",},
        nextlink:  {__SPEC:false, DEFAULT: "", TYPE: "(String|Function)",},
        scriptline:{__SPEC:false, DEFAULT: "", TYPE: "(String|Function)",},
        firstline: {__SPEC:false, DEFAULT: cbkNoteName, TYPE: "(String|Function)",},
      },
    },
	 note:{ 
      schoolyaml: { },
      schoolshow: { },
    },
	werkstattmitschrift: { 
      folders: ["Werkstatt/Mitschriften"],
      marker: "@",
      name_prompt: "Titel der Veranstaltung",
      schoolyaml: {
        author: "",
        cssclasses: "studies",
        publish: false,
      },
      schoolshow: {
        firstline: "Mitschrift",
      },
    },
     mitschrift: { 
      folders: ["Werkstatt", "Buchmitschriften"],
      marker: "@",
      name_prompt: "Autornachname - Buchtitel",
    },
    buch: {
      folders: ["Werkstatt"],
      marker: "{b}",
      name_prompt: "Autornachname - Buchtitel",
      title_date_function: cbkAskGoogleForTitle,
      schoolyaml: {
        buchtitel: cbkBuchTitel,
        buchautor: cbkBuchAutor,
        buchdatum: cbkBuchDatum,
        buchstatus: [ "gelesen", ],
        xbuchstatus: [ "aktuell", "teilweise", "nochmal", "ungelesen", ],
      }
    },
  },
}
```
Der Default NoteType ist note - wird das nicht angegeben, ist es der erste.
Die Defaultsbereiche heissen hier schoolyaml und schoolshow - die Namen sind egal, in den NotyTypes müssen dann aber diese Namen verwendet werden. Der YAML Eintrag cssclasses wird durch die Funktion cbkFmtCC bestimmt. Die muss es geben, sonst bricht das Script mit einem Fehler ab. Der author und publish werden auf feste Werte gesetzt. 

Für den Renderbereich werden die Einträge prevlink und nextlink und scriptline mit einem leeren Wert vorgegeben und firstline bekommt wieder den Notiznamen ohne Marker von einer Funktion.

Der Default NoteType note übernimmt alles wie oben vorgegeben. die beiden mittleren Zeilen könnten auch fehlen.

Der NoteType werkstattmitschrift wird bei neuen Notizen in Verzeichnissen "Werkstatt/Mitschrift angewandt. Vor den Notiznamen wird ein Klammeraffe gestellt. Der Autor wird als leer überschrieben, publish mit false und firstline mit "Mitschrift".

Der NoteType mitschrift wird in Verzeichnissen "Werkstatt" und "Buchmitschriften" erstellt (und in deren Unterverzeichnissen, falls nicht eine Regel greift die näher am letzten Teil des Pfades ist). Der Marker ist auch ein Klammeraffe. Alle Vorgaben werden übernommen.

Auch der NoteType buch wird in Werkstatt erzeugt. Sein Marker ist {b}, Es werden also Namen erzeugt wie: "{b}Kant - Vernunft". Die Funktion cbkAskGoogleForTitle geht ins Netz und frägt Google nach Büchern mit den Stichwörtern, die beim name_prompt eingegeben wurden (also z.B. Kant und Vernunft). Aus der von Google zurückgegebenen Liste lässt sie den Nutzer dann einen auswählen. Die erhaltenen Informationen braucht sie teilweise selbst für den Dateinamen und sie speichert sie auch zwischen, für die anderen Callbackfunktionen. cbkBuchTitel, cbkBuchAutor und cbkBuchDatum greifen darauf zu und geben damit ihre Werte zurück. 

Der Buchstatus kann einen von  5 Werten haben. Die anderen vier kommen in ein Bequemlichkeitsarray, so dass man sie beim Ändern des Wertes einfach kopieren kann.

### Anmerkungen zur Verwendung in Obsidian
- Obwohl man den Notiznamen für eine neue Notiz im Dialogprompt angegeben hat, muss man noch `<return>` drücken. Dies ist kein Fehler des Scripts. Eventuell ist es eine Regression, jahrelang davor ist es mir nicht negativ aufgefallen.
- Wenn man in den Einstellungen im Abschnitt  `Appearance` sowohl `Show inline title` als auch die folgende Einstellung `Show tab title bar` ausschaltet poppt bei der namenlosen Neuerstellung einer Notiz zusätzlich zum Dialog des Templates noch ein Dialog von Obsidian auf, der auch einen Dateinamen will.
  - Die [Lösung des doppelten Dialog Problems](https://forum.obsidian.md/t/templater-triggering-before-choosing-files-title/52968/11) ist  `Show tab title bar` anzuwählen; der Thread in dem diese Lösung auftaucht, beschreibt das Problem. Scheinbar hat sich das seit 2023 nicht geändert. 
  - Meine Lösung ist zusätzlich `.view-header` im css möglichst klein und unsichtbar zu machen, aber nicht mit `display:none` , was einem Ausschalten von `Show tab title bar` entspräche.
### github.io
- Github hosted mit dem Service [Github Pages](https://docs.github.com/de/pages) zu jedem Account eine statische Webseite. 
- Das Github Projekt, das diese Seite definiert muss `accountname.github.io` heißen.
- Früher hieß der gesamte Service github.io, heute heißt er Github Pages.
- Github läuft seit über einem Jahrzehnt auch für kostenlose Konten stabil und problemlos
- Verzeichnisse und Dateien dürfen nicht mit einem Unterstrich beginnen
- Ein Minuszeichen würde gehen, macht aber Zugriff über [bash](https://de.wikipedia.org/wiki/Bash_(Shell)) komplizierter
- Dateinamen dürfen mit einem Klammeraffen `@` oder einer Ziffer beginnen  
%%
tote externe Links checken: https://error404.atomseo.com/
%%
## -footnotes

[^1]: so nennt Obsidian Notizbücher 
[^2]: Add 2 spaces at the start of each new line.
  This lets you write footnotes that span multiple lines.
  

