---
cssclasses: note
date_created: 2025-11-24
publish: true
author: Ueberphilosophy
---
# Mit den Ohren lernen
Sammlung von Links zu __Materialien__ zum Lernen (hörbar) __[[-Materialien|als Katalog]]__/__[[Materialien|als Verzeichnis]]__  und frei zugänglichen __Quelltexten__ __[[Materialien/timeline|als  Zeitleiste]]__/__[[Autoren|als Verzeichnis]]__. 

Diese befindet sich als kaum kommentierte Linksammlung im Ordner `Materialen`. Der Ordner `Werkstatt` kann für jeweils eigene Notizen verwendet. Im Ordner `Zusaetze` sind für die Sammlung unwichtige Seiten. Die selbst erstellen Definitionen im Ordner `Zusaetze/Definitionen` sind grob, auf den Themenseiten im Ordner `Zusaetze/Themen` finden sich Links zu bestimmten Themen.  
## Bedienung
 - Klick vor (links neben) Überschriften klappt den Inhalt ein, nochmaliger Klick wieder auf; das zugehörige Symbol wird beim Drüberfahren mit der Maus sichtbar. 
 - Ganz oben links und rechts kann man die Seitenleisten ein- und ausblenden
 - Auf der rechten Seitenleiste oben kann man dunkle oder helle Anzeige einstellen.
 - Im Suchfeld auf der linken Seitenleiste oben durchsucht man alle Seiten. Nach Tags sucht man mit vorrangestelltem Doppelkreuz: `#tagname`. 
 - Beim  Klick mit der Maus öffnen alle Links, auch externe,  im selben Fenster. `Ctrl` (deutsch: `Shift`)-Klick öffnet in einem neuen Tab.
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
Es wird unterschieden zwischen Lernmaterialen, hauptsächlich Videos und Audios,  und Quellen. Lernmaterialen sind über ein Thema, Quellen sind  frei zugängliche Originaltexte. Für Lernmaterialien gibt es einen  [[-Materialien|Katalog]] nach Bereichen. Quellen sind nach Autoren unterschieden, sie sind über die [[Materialien/timeline|Zeitleiste]]  zu finden. Der Katalog wird automatisch erstellt, die timeline manuell. Beide Bereiche sind auch über das [[Materialien|Inhaltsverzeichnis]] zugänglich. Über die Seitenleiste links kann man alle Seiten finden. Die Dateinamen der Kataloge beginnen mit einem Bindestrich, die Dateinamen der Inhaltsverzeichnisse heissen wie die Verzeichnisse, die sie auflisten.


- Grobe [[Materialien/timeline|Zeitleiste]]  mit Links zu Quellenseiten (verknüpft über den Autorennamen)
- [[-Materialien|Katalog]] mit Links zu thematischen Sammlungen von  Links zu Lernmaterialen
## Netzresourcen
### Seiten für Quellen
- [Gottwein](https://www.gottwein.de/7)
- [12koerbe](http://12koerbe.de/)
- [Perseus](https://www.perseus.tufts.edu/hopper/)
- [librivox](https://librivox.org/)
- [Internet Archive](https://archive.org/)
- [zeno](http://www.zeno.org/)
- [Projekt Gutenberg](https://www.projekt-gutenberg.org/)
- [Wikisource](https://wikisource.org/wiki/Main_Page)
- [Google Books](https://books.google.de/)
- [jstor](https://www.jstor.org/)
- [Deutsches Textarchiv](https://deutschestextarchiv.de/)
- [Österreichische Nationalbibliothek](https://onb.digital/)
- [Standard E-Books](https://standardebooks.org/)
- [Französische Nationalbibliothek](https://www.bnf.fr/en) 
- [Münchener Digitalisierungszentrum](https://www.digitale-sammlungen.de/de)
- [Bibliothek Uni Halle](https://halit.bibliothek.uni-halle.de/search?q=&v=)
- [biblotheca augusthana](https://www.hs-augsburg.de/~harsch/augustana.html)
- [Herzogin Anna Amalia Bibliothek](https://haab-digital.klassik-stiftung.de/viewer/index/)
- [Internet History Sourcebooks Project](https://sourcebooks.fordham.edu/index.asp)
- [Logos Verlag Open Access](https://www.logos-verlag.de/cgi-bin/mylibrary)
- [Marxist Internet Archive](https://www.marxists.org/index.htm)
- [Hegel Werke](https://hegel.net/hegelwerke/)
- [Psychoanalytische Bibliothek Berlin](https://psybi-berlin.de/literatur-online/)
- [oapen](https://oapen.org/)
- [de Gruyter open access](https://library.oapen.org/browse?type=publisher&value=De+Gruyter)
- [Logos Verlag Open Access Verzeichnis](https://www.logos-verlag.de/ebooks/OA/)
%% 
- [Annas Archive](https://annas-archive.org/) Schattenarchiv, Grauzone, manchmal illegal
- https://dokumen.pub/  Bücher mit Copyright Verletzungen und evlt Malware 
- [Zeitungsartikel archive.ph](https://archive.ph/)
- [odysseetheater](https://odysseetheater.org/ftp/) Weiss nicht ob die legal oder beständig sind
%% 
### Kanäle für Materialen
#### Sammlungen von Kanälen
- [Uni Frankfurt Portalsammlung](https://okapi.uni-frankfurt.de/index.php/Philosophie_Multimedial)
- [Vorlesungssammlung Philosophie](https://www.edukatico.org/de/online-kurse/philosophie)
- [Philosophiechannels auf YouTube](https://griffl.org/die-besten-philosophie-channels-auf-youtube/)
- [30 Quellen für Onlinevorlesungen aller Fachbereiche](https://www.fernstudi.net/magazin/10963)
- [Wissenschaftspodcasts](https://wissenschaftspodcasts.de/)
- [Philosophie Blogs](https://www.information-philosophie.de/blogs.html)
#### Kanäle Philosophie
- [LMU Videos von Vorlesungen und Vorträgen Philosophie](https://www.philosophie.lmu.de/de/medien/videos-von-vorlesungen-und-vortraegen/)
- [Uni Hannover Philosophie Vorlesungsaufzeichnungen](https://www.philos.uni-hannover.de/de/studium/lehrveranstaltungen/videos)
- [Uni Tübingen kath-theol Fakultät Vorlesungen als Videos](https://uni-tuebingen.de/fakultaeten/katholisch-theologische-fakultaet/lehrstuehle/philosophische-grundfragen-der-theologie/vorlesungen-als-video/)
- [TU Darmstadt Philosophie Audiothek](https://www.philosophie.tu-darmstadt.de/institut_phil/audiothek_phil/index.de.jsp)
- [Philosophische Audiothek Uni Wien](https://audiothek.philo.at/) - [Sitemaps](https://audiothek.philo.at/sitemap.xml)
- [Philosophie Uni Stuttgart](https://www.youtube.com/@institutfurphilosophieuniv5984/featured)
- [Finkelde YouTube](https://www.youtube.com/@dominikfinkelde/videos) 
- [Online Vorlesungen Philosophie des Geistes](https://www.online-vorlesungen.de/Videos/Philosophie/Philosophie_des_Geistes.htm)
#### Andere Bereiche
- [LMU Psychologie/Pädagogik - einige frei](https://videoonline.edu.lmu.de/de/semester)
- [Uni Düsseldorf Mediathek](https://mediathek.hhu.de/)
- [Uni Hamburg Lecture2Go Videokatalog](https://lecture2go.uni-hamburg.de/l2go)
- [Alexander Lasch Linguistik YouTube](https://www.youtube.com/@AlexanderLasch/featured)
- [Elena Smirnova Sprachwissenschaft YouTube](https://www.youtube.com/@elenasmirnova674/featured)
- [Lacan Podcast](http://lacast.de/) und [Lacan Videos](https://lacan-entziffern.de/category/video-lacan-entziffern/)
- [ARD Radiowissen](https://www.ardaudiothek.de/sendung/radiowissen/urn:ard:show:a5369fa8556fcd7b/)
### Datenbanken für alle Medien
- [Datenbank Infosystem](https://dbis.ur.de/browse/subjects/31/)
%%https://transformatorische-bildung.de/ %%
## Technisches über diese Site
### Einstellungen
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
    - Default location for new notes: Same folder as current file
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
       - Backlinks aus
       - Tags Feature Placement `Start` von `.footer .data-bar` 
       - RSS aus
- Editmode angepasst mit eigener Datei `obsidian-source-view.css`. 
- Export angepasst in eigener Datei  `adapt.css`. 
- dort auch die css Klassen definiert
- Eigenes Script `foty.js` nach `allhelperfiles/allscripts`, ^Script
- Eigenes Template `foty_Vorlage.md` nach `allhelperfiles/allvorlagen`. ^Vorlage
- Plugin [Templater](https://github.com/SilentVoid13/Templater) erstellt neue Notes mit [[home#^Script|Script]] `allhelperfiles/allscripts/foty.js` und [[home#^Vorlage|Vorlage]] `allhelperfiles/allvorlagen/foty_Vorlage.md`
  - Einstellungen Templater
    - Template Folder Location `allhelperfiles/allvorlagen`
    - automatic jump to cursor, 
    - Trigger Templater on new file creation, 
    - Kein enable folder templates, 
    - Enable file regex template
    - file regex template `allhelperfiles/allvorlagen/foty_Vorlage.md`, 
    - Script files folder location `allhelperfiles/allscripts`
- Plugin [Dataview](https://blacksmithgu.github.io/obsidian-dataview/)
  - Einstellungen Dataview
    -  Enable Javascript Queries
- Plugin [Shortcuts Extender](https://github.com/ryjjin/Obsidian-shortcuts-extender) ^[Nur wegen des Backticks für Code, insbesondere des dreifachen Backticks für Code Blöcke]
- Plugin [ProZen](https://github.com/cmoskvitin/obsidian-prozen)
- Plugin [Typewriter Mode](https://github.com/davisriedel/obsidian-typewriter-mode)
- Plugin [Vimrc](https://github.com/esm7/obsidian-vimrc-support) 
- Plugin [Waypoint](https://github.com/IdreesInc/Waypoint) ^[zum Erstellen der Inhaltsverzeichnisse]
- Plugin [Foldernotes](https://github.com/LostPaul/obsidian-folder-notes) ^[für die Eingliederung der Verzeichnisseiten in Obsidian]
  - Einstellungen
    - File Explorer
      - Open Folder Notes by only clicking directly on the folder name anwählen
- Für Zeitleiste [Timeline Callout von FirelsGood](https://github.com/r-u-s-h-i-k-e-s-h/Obsidian-CSS-Snippets/blob/Collection/Snippets/Callout%20styling%20-%20Timeline%20callout.md), leicht angepasst, als `timeline.css`. 
%%
- Plugin [Folder notes](https://github.com/LostPaul/obsidian-folder-notes)
  - Einstellungen Folder notes
    - Abschnitt Folder Overview
      - Folder path of the Overview: "Path of folder linked to the file"
	- Abschnitt File Explorer
	  - Open folder notes by only clicking directly to the folder name an
	  - Disable folder collapsing aus
%%
### Formatierungen
#### Basics
siehe Obsidian [Basic Formatting Syntax](https://help.obsidian.md/syntax)
- __bold__ *schräg* ~~Durchgestrichen~~ ==Highlight== ***Fett Schräg***  ***==Fett Schräg Highlight==*** ^textformate
- [[home#^zitat|Zitate]], beginnend mit \> 
- Listen, wie diese, auch geschachtelt
- 1) und auch,
- 2) nummerierte Listen
- sowie Aufgaben
- - [x] erledigt
- - [ ] offen
-  Tags, z.B. #Argumente , auch geschachtelte Tags wie #speaker/Jaspers-Karl 
- Inline `code` und Codeblöcke mit \`\`\` umschlossen
- Fußnoten direkt im Text^[Nach einem Dach steht der Fussnotentext in eckigen Klammern] und  mit `[^zahl]` längere Fußnoten[^2] (keine Hover-Anzeige  von Fußnoten mit `Webpage HTML Export`)
- internes und externe Links (Benutze auch Wiki-Links)
- Bilder anzeigen mit \!\[\]\(link\), in Größe 250  mit  \!\[\|250\]\(link\)
- Absatz (Leerzeile beendet Absatz)
- mehrere Leerzeichen verschwinden zu einem 
- Neue Zeile verschwindet, außer zwei Leerzeichen sind vorm Zeilenumbruch
- Überschriften (# bis ###### )
- Links zu [[home#Sammlungen von Kanälen|Überschriften auf selber Seite]], auf anderer Seite funktioniert [[DDCKlassen#723|723 nur in Obsidian, im Export normalerweise nicht]], außer auf anderer Seite ist der Link  als [[DDCKlassen#723_0|723_0 für den Export angepasst]]
- Trennlinie mit drei \-\-\-
- Kommentare innerhalb von \%\%, die nicht exportiert werden - %%sieht man nicht%% -

> Human beings face ever more complex and urgent problems, and their effectiveness in dealing with these problems is a matter that is critical to the stability and continued progress of society. ==-Doug Engelbart, 1961== ^zitat
```
dies ist ein codeblock
§$-?*+^ 

```
#### Weitergehende Formatierungen
siehe Obsidian [Advanced Formatting Syntax](https://help.obsidian.md/advanced-syntax) und folgende Seiten für
- Tabellen
- Mermaid Diagramme
- Mathematische Ausdrücke innerhalb  \$-Zeichen inline $e^{2i\pi} = 1$ oder Paaren von \$\$-Zeichen als Block
- Anker, Links zu [[home#^textformate|Ankern]], sowie Linknamenüberschreibungen
- Callouts
- Tags #tag und Nested Tags #nested/tag - Groß/Kleinschreibung ist für Tags egal

> [!quote]- Das ist ein Callout Block
> Durch ein Pluszeichen wäre er ursprünglich aufgefaltet. So wird er gefaltet angezeigt.
>
> Es gibt folgende Callouts: Note, Abstract, Info, Todo, Tip, Success, Question, Warning, Failure, Danger, Bug, Example, Quote - alle kleingeschrieben, aber groß angezeigt, falls der Titel nicht überschrieben wird

### Obsidian 
Dieser Abschnitt gilt nur für  eine laufende Obsidian Instanz

- Obwohl man den Notiznamen für eine neue Notiz im Dialogprompt angegeben hat, muss man noch `<return>` drücken. Dies ist kein Fehler des Scripts. Eventuell ist es eine Regression, jahrelang davor ist es mir nicht negativ aufgefallen.
- Wenn man in den Einstellungen im Abschnitt  `Appearance` sowohl `Show inline title` als auch die folgende Einstellung `Show tab title bar` ausschaltet poppt bei der namenlosen Neuerstellung einer Notiz zusätzlich zum Dialog des Templates noch ein Dialog von Obsidian auf, der auch einen Dateinamen will.
  - Die [Lösung des doppelten Dialog Problems](https://forum.obsidian.md/t/templater-triggering-before-choosing-files-title/52968/11) ist  `Show tab title bar` anzuwählen; der Thread in dem diese Lösung auftaucht, beschreibt das Problem. Scheinbar hat sich das seit 2023 nicht geändert. 
  - Meine Lösung ist zusätzlich `.view-header` im css möglichst klein und unsichtbar zu machen, aber nicht mit `display:none` , was einem Ausschalten von `Show tab title bar` entspräche.
#### tote interne Links
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

[^2]: Add 2 spaces at the start of each new line.
  This lets you write footnotes that span multiple lines.

