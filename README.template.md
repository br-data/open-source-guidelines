# README-Vorlage

Die Markdown-Vorlage soll dabei helfen bessere README-Dateien zu schreiben. Eine gut geschriebene Dokumentation vermittelt Kompetenz und hilft dabei Code und Datenanalysen besser zu verstehen.

- **Demo:** [Original README-Vorlage bei Github](https://github.com/digitalegarage/open-source-guidelines/blob/master/README-template.md)

## Datenquelle

Dieses README baut auf den Ideen von Stephen Whitmore's [Art of README](https://github.com/noffle/art-of-readme) auf.

## Abhängigkeiten

Dieses Readme ist in [Markdown](https://guides.github.com/features/mastering-markdown/) geschrieben. Um es zu bearbeiten reicht ein einfacher Text-Editor wie [Sublime Text](https://www.sublimetext.com/). Um eine HTML-Vorschau zu erzeugen benötigt es allerdings ein Plugin wie [sublimetext-markdown-preview](https://github.com/revolunet/sublimetext-markdown-preview). Eine Liste anderen Markdown-Editoren gibt es [hier](https://github.com/karthik/markdown_science/wiki/Tools-to-support-your-markdown-authoring).

## Verwendung

1. Repository klonen `git clone https://...`
2. README bearbeiten `subl README.md`
3. Änderungen einchecken `git add README.md` und committen `git commit -m "Update README"`

## Funktionen

Tipps, um semantische READMEs mit Markdown zu schreiben. Ein vollständige Dokumentation der Funktionen bietet das [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet).

### Textformatierung

Hervorhebungen lassen sich in Markdown folgendermaßen gestalten:

- **Text fett**: `**fett**`
- *Text kursiv*: `*fett*`

Außerdem gibt es verschiedene Überschriften:

# H1
## H2
### H3
#### H4
##### H5
###### H6

Die Überschriften unterscheiden sich jeweils durch die Anzahl der vorangestellten Rauten `## H2`.

### Aufzählungen

Markdown bietet die Möglichkeit verschiedene Aufzählungen anzulegen.

Unsortierte Aufzählungen mit vorangestellten Bindestrichen `-`:

- Listeneintrag
- anderer Listeneintrag
- noch ein Listeneintrag

Sortierte Aufzählung mit vorangestellten Zahlen `1.`:

1. Erster Listeneintrag
2. Zweiter Listeneintrag
3. Dritter Listeneintrag

### Links und Bilder

Links bestehen jeweils aus einem Linktext und einer URL `[Linktext](http://github.com/br-data)`.

Beispiel: [Zur README-Vorlage](https://github.com/digitalegarage/open-source-guidelines/blob/master/README-template.md)

Bilder können nach dem gleichen Prinzip eingebunden werden. Einziger Unterschied ist das führende Ausrufezeichen `![Bildbeschreibung](https://de.wikipedia.org/wiki/Datei:GitHub_logo_2013.svg)`

![Github-Logo](https://de.wikipedia.org/wiki/Datei:GitHub_logo_2013.svg)

### Code

Unformatierte Codefragmente können im Paragraphen mit Backticks `this.function()` angezeigt werden oder als ganze Code-Blöcke mit drei Backticks in der ersten und letzten Zeile. Für passendes Syntax-Highlighting muss in der ersten Zeile die Skriptsprache angegeben werden `javascript`.

Beispiel:

```javascript
function add(a, b) {
  return a+b
}

add(1, 2) // returns 3
```

## Probleme

Manchmal funktioniert der Markdown-Renderer nicht. In diesem Fall hilft meistens ein Neustart des Text-Editors.

## Verbesserungen

- Beispiel-Readme auf Englisch hinzufügen
- Einstellungen im Text-Editor ausführlicher beschreiben

## Dank und Quellen

- Philosophie: [Art of README](https://github.com/noffle/art-of-readme)
- Markdown-Beispiele von [Github Markdown](https://guides.github.com/features/mastering-markdown/) und [Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
