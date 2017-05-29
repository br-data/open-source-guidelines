# Open Source bei BR Data
Ein paar Empfehlungen zum Veröffentlichen von bestehenden Projekten auf Github. Grundsätzlich versuchen wir alle Projekte zu veröffentlichen, die es unseren Benutzen ermöglichen Rechercheweg und Datenanalyse hinter einer Geschichte zu verstehen und zu verifizieren (Transparenz). Ferner sind wir bereit zu unseren Fehlern zu stehen und diese gegebenenfalls auszubessern. Im Idealfall können die von uns entwickelten Programme und Analysen von der Datenjournalismus-Community weiter genutzt und verbessert werden. 

_„Open Source ist kein Dogma, sondern eine partizipative Kultur der Offenheit und des Teiles. Denn am Ende konkurrieren wir (Journalisten) nicht um das beste Werkzeug, sondern um die beste Geschichte.“_

## Unterschiedliche Projektarten
Verschieden Projekte stellen unterschiedliche Anforderungen an die Veröffentlichung. Oftmals überschneiden sich die Projektarten auch oder sind am besten in einem Repository zusammenzufassen:

- **Datenanalysen:** Bei Datenanalysen geht es vor allem darum die einzelnen Schritte der Analyse transparent und reproduzierbar gestalten.
- **Datensätze:** Es sollten vor allem Datensätze veröffentlicht werden, die anderweitig schwer zu bekommen sind. Zum Beispiel Datensätze, welche von einer Behördenseite befreit wurden (z.B. durch einen Scraper). Wichtig: Urheberrechte abklären.
- **interaktive Grafiken:** Besondere interaktive Grafiken, welche mit hohem Aufwand erstellt wurden und die man auf andere Themen anwenden könnten. Beispiel: Netzwerk-Visualisierungen. 
- **Tools:** Allgemeine Werkzeuge die bei einem bestimmten, verallgemeinerbaren Workflow helfen. Beispiel: PDFs herunterladen, in Text umwandeln, in eine Datenbank importieren. Dabei geht es vor allem häufige Aufgaben zu automatisieren.
- **(Web-)Anwendungen:** Größere Software-Projekte, welche einen verallgemeinerbaren Nutzen haben. 

## Zielgruppe definieren
Vor allem für das Readme und die Dokumentation ist es wichtig sich zu überlegen, für wen man eigentlich schreibt. Generell hilft es immer von sich selbst in zwei Jahren oder einem Kollegen der noch nichts mit dem Projekt zu tun hatte auszugehen. Die Person beherrscht zwar die Grundlagen der Programmierung oder Datenanalyse, weiß aber nichts (mehr) über die Eigenheiten und Details des Projekts. Es macht wenig Sinn, Software- oder Datenanalyseprojekte so zu dokumentieren, dass sie eine absoluter Laie verstehen würde.

## README schreiben
Die Readme-Datei ist der zentrale Einstiegspunkt in ein jedes Projekt. Ein gut geschriebenes Readme erleichtert den Einstieg in ein Projekt und vermittelt Kompetenz und Ernsthaftigkeit. Im Idealfall umfasst das Readme:  

- **Projekttitel:** Um was geht es bei dem Projekt?.  
- **Projektbeschreibung:** Welche Funktionen oder Erkenntnisse (bei Analysen) bietet das Projekt? Was macht das Projekt besonders?.    
- **Demo- oder Artikellink:** Wie sieht das Projekt aus, wenn alles funktioniert? Wie fühlt sich die Benutzeroberfläche an?
- **Datenquelle:** Woher kommen die Daten und wie kann ich sie verwenden (Copyright)?
- **Abhängigkeiten:** Was brauche ich zusätzlich, um das Projekt zum laufen zu bekommen (z.B. Python 2.7 und PostgreSQL)?
- **Verwendung:** Was muss ich machen, um das Projekt zu verwenden? 
- **Funktionen:** Welche Funktionen (oftmals Skripten) hat das Projekt und wie verwende ich diese im Detail?
- **Probleme:** Welche häufigen Probleme gibt (und wie gehe ich damit um)? 
- **Roadmap:** Wo steht das Projekt und wo soll es mal hin?
- **Dank und Quellen:** Wer hat zum dem Projekt beigetragen, wovon wurde das Projekt inspiriert?

**Wie umfangreich sollte das Readme sein?** In das Readme gehören alle Informationen die unmittelbar notwendig sind, um das Projekt zu verwenden. Details, wie man eine bestimmte Datenbank aufsetzt, muss man nicht ausführen. Hier reicht ein Link oder zumindest der Hinweis das die Installation einer bestimmten Datenbank vorausgesetzt wird (Stichwort Anforderungen). 

## Dokumentation und Kommentare
Die Dokumentation im Code sollte zielführend und dem Umfang des Projekts angemessen sein. Am wichtigsten sind aber sprechende Variablen-, Funktions- und Klassennamen. Wenn eine Funktion `toDashCase(string)` heißt, muss man eigentlich nicht mehr viel kommentieren. Oft ist es wichtiger die zu erwartenden Parameter zu beschreiben. Hier sollte man gängige Konventionen wie [JSDoc](http://usejsdoc.org/) oder [pydoc](https://docs.python.org/2/library/pydoc.html) befolgen:

```javascript
/**
 * @param {string} Word or sentence
 */

function toDashCase(string) {
  
  return string.replace(/\s+/g, '-').toLowerCase()
}
```

## Lizenz hinzufügen
Damit andere Benutzer den Code für ihre eigenen Projekte nutzen können, braucht das Repository einen Lizenz:

1. Auf der Github-Projektseite **Create new file** auswählen.
2. Als Name der Datei `LICENSE` eingeben.
3. Vorlage **MIT** aus der Liste rechts auswählen.
4. Copyright-Zeile in `Copyright (c) 2017 Bayerischer Rundfunk` ändern.
5. Unten auf der Seite eine Commit-Beschreibung `Add license` eingeben und bestätigen.

**Warnung:** Wichtig ist, dass die Urheberrechte für alle im Repository enthaltene Inhalte (Code, Text, Daten, Schriften, Bilder ...) beim Bayerischen Rundfunk liegen. Fremdinhalte wie Software-Bibliotheken sollten immer über einen Paketmanager ([npm](https://www.npmjs.com/), [yarn](https://yarnpkg.com/), [pip](https://pypi.python.org/)) installiert werden.

## Einstellungen anpassen
Für viele kleinere Projekte ist nicht davon auszugehen, dass sich darum einen Community bilden wird. Die Veröffentlichung dient dabei eher der Transparenz als der Nutzbarmachung. Daher kann man sich überlegen, ob man folgende Optionen in den Projekteinstellungen (Github-Settings > Options) auszuschaltet:

- **Wikis**: Eher für die ausführliche Projektdokumentation gedacht. 
- **Issues**: Benutzer und Kollegen können Fehler melden und sich Funktionen wünschen.
- **Projects**: Kanban-Board, Todos und Milestones für größere Projekte.  

Wenn man diese Optionen aktiviert, sollte man auch bereit sein, Zeit in die Bearbeitung von Benutzerwünschen und Bugs zu investieren.

## Projekt veröffentlichen
Das Veröffentlichen geschieht über die Github-Settings > Options:

1. Projekt veröffentlich: **Make this repository public**
2. Eigentumsrechte auf `br-data` übertragen: **Transfer ownership**

Das Übertragen der Eigentumsrechte kann einige Minuten dauern.

## Lokales Projekt anpassen
Wenn man das Repository bereits aus dem eigenen Rechner ausgecheckt hat, muss man den Remote-URL anpassen. Vergisst man die die Remote-URL anzupassen kann man nicht mehr Pushen und Pullen. Die neue URL bekommt man in dem man auf der Github-Projektseite auf **Clone or download** geht. Es empfiehlt sich immer den SSH-Link zu kopieren (statt des HTTPS-Links).

Die Remote-URL kann man mit folgendem Kommandozeilenbefehl ändern:

```
$ git remote set-url origin git@github.com:br-data/mein-repo.git
```

Um zu überprüfen, ob die Änderung geklappt hat, kann man sich die Remote-URL mit folgendem Befehl anschauen:

```
$ git remote -v
origin	git@github.com:br-data/mein-repo.git (fetch)
origin	git@github.com:br-data/mein-repo.git (push)
```

## Passwörter entfernen
Manchmal hat man versehentlich Passwörter, API-Keys oder andere vertrauliche Informationen in einem Repo eingecheckt. Diese sollte man unbedingt vor Veröffentlichung des Projektes entfernen. Am einfachsten geht das mit dem [BFG Repo Cleaner](https://rtyley.github.io/bfg-repo-cleaner/). Es empfiehlt sich das Projekt vorher zu sichern. 

Als erstes muss das Repository gespiegelt werden: 

```
$ git clone --mirror git@github.com:digitalegarage/mein-repo.git
```

Möglichkeit A: Alle Dateien löschen die *id_rsa* oder *id_dsa* heißen:

```
$ bfg --delete-files id_{dsa,rsa} mein-repo.git
```

Möglichkeit B: Alle Dateien nach Passwörtern aus einer Liste durchsuchen und mit `***REMOVED***` ersetzen:

```
$ bfg --replace-text passwords.txt mein-repo.git
```

Um folgende Befehle auszuführen muss man in das Verzeichnis wechseln:

```
$ cd mein-repo.git
```

Alle Referenzen aktualisieren und alte Referenzen löschen:

```
$ git reflog expire --expire=now --all && git gc --prune=now --aggressive
```

Referenzen pushen.

```
$ git push
```

**Warnung:** Sobald Passwörter in ein öffentliches Repository eingecheckt wurde, sollte man sie als kompromittiert betrachten. In diesem Fall hilft es nur, die betroffenen Passwörter auszutauschen. API-Keys und Auth-Tokens müssen neu generiert werden.

**Vorsorge:** Um zu verhindern, dass sensible Daten eingecheckt werden, sollte man vorsichtig mit globalen Kommandos wie `git add -A` umgehen. Besser ist es Dateien einzeln zu einem Commit hinzuzufügen. Auf jeden Fall sollten vor einem Commit noch einmal die vorgeschlagenen (staged) Dateien angeschaut werden: `git status`. Um ein versehentliches Einchecken zu verhindern, kann man sensible Konfigurationsdateien auch zur `.gitignore` hinzufügen.

