# Open Source bei BR Data

Ein paar Empfehlungen zum Veröffentlichen von bestehenden Projekten auf Github. Grundsätzlich versuchen wir, alle Projekte zu veröffentlichen, die es unseren Benutzen ermöglichen, Rechercheweg und Datenanalyse hinter einer Geschichte zu verstehen und zu verifizieren (Transparenz). Wir sind bereit, zu unseren Fehlern zu stehen und sie gegebenenfalls auszubessern. Im Idealfall können die von uns entwickelten Programme und Analysen von der Datenjournalismus-Community weiter genutzt und verbessert werden.

*„Open Source ist kein Dogma, sondern eine partizipative Kultur der Offenheit und des Teiles. Denn am Ende konkurrieren wir (Journalisten) nicht um das beste Werkzeug, sondern um die beste Geschichte.“*

## Inhalt

- [Unterschiedliche Projektarten](#unterschiedliche-projektarten)
- [Zielgruppe definieren](#zielgruppe-definieren)
- [Deutsch oder Englisch?](#deutsch-oder-englisch)
- [Projekt benennen](#projekt-benennen)
- [README schreiben](#readme-schreiben)
- [Dokumentation und Kommentare](#dokumentation-und-kommentare)
- [Commit-Messages](#commit-messages)
- [Passwörter entfernen](#passwörter-entfernen)
- [Badges](#badges-hinzufügen)
- [Lizenz hinzufügen](#lizenz-hinzufügen)
- [Einstellungen anpassen](#einstellungen-anpassen)
- [Projekt veröffentlichen](#projekt-veröffentlichen)
- [Lokales Projekt anpassen](#lokales-projekt-anpassen)
- [Gute Beispiele](#gute-beispiele)
- [Kontakt](#kontakt)

## Unterschiedliche Projektarten

Verschieden Projekte stellen unterschiedliche Anforderungen an die Veröffentlichung. Oftmals überschneiden sich die Projektarten und lassen sich auch in einem Repository zusammenzufassen:

- **Datenanalysen:** Bei Datenanalysen geht es vor allem darum, die einzelnen Schritte der Analyse transparent und reproduzierbar gestalten.
- **Datensätze:** Es sollten vor allem Datensätze veröffentlicht werden, die anderweitig schwer zu bekommen sind. Zum Beispiel Datensätze, die von einer Behördenseite befreit wurden (z.B. durch einen Scraper). Wichtig: Urheberrechte abklären.
- **interaktive Grafiken:** Auch interaktive Grafiken und Anwendungen, welche man auf ein anderes Themen anwenden könnte und die aufwändig erstellt wurden, sollten veröffentlicht werden. Beispiel: Wahlkarten, Netzwerk-Visualisierungen.
- **Tools:** Allgemeine Werkzeuge, die bei einem bestimmten, verallgemeinerbaren, Workflow helfen. Beispiel: PDFs herunterladen, in Text umwandeln, in eine Datenbank importieren. Dabei geht es vor allem darum, häufige Aufgaben zu automatisieren.
- **(Web-)Anwendungen:** Größere, aufwendige Software-Projekte, die einen verallgemeinerbaren Nutzen haben.

## Zielgruppe definieren

Vor allem für das Readme und die Dokumentation ist es wichtig, sich zu überlegen, für wen man eigentlich schreibt. Generell hilft es immer, von sich selbst in zwei Jahren, oder einem Kollegen, der noch nichts mit dem Projekt zu tun hatte, auszugehen. Die Person beherrscht zwar die Grundlagen der Programmierung oder Datenanalyse, weiß aber nichts (mehr) über die Eigenheiten und Details des Projekts. Es macht wenig Sinn, Software- oder Datenanalyseprojekte so zu dokumentieren, dass selbst eine absoluter Laie sie verstehen kann.

## Projekt benennen

Dinge kurz und verständlich zu benennen ist eine Herausforderung, vor allem wenn es dabei um den Namen eines neuen Github-Repositories geht. Wir benennen unsere Repositories nach folgendem Schema:

```text
(jahr)-titel-typ
```

Projekte bekommen nur dann eine **Jahreszahl**, wenn sie in einem bestimmten Jahr abgeschlossen und veröffentlicht wurden. Meistens sind das Datenanalysen oder Recherchen. Anleitungen, Services und Werkzeuge bekommen keine Jahreszahl, da sie laufen weiterentwickelt werden.

Der **Titel** sollte sprechend sein und das Thema möglichst kurz und genau beschreiben. Der Titel kann mehrere Wörter enthalten, diese sollten jedoch ebenfalls kleingeschrieben und durch einen Bindestrich getrennt werden.

Als letztes wird der **Typ des Repositories** angegeben. Gute Suffixe sind:

- **-analyse**: Datenanalyse oder -auswertung
- **-longread**: Artikel mit interaktiven Elementen
- **-chart**: Grafik oder Datenvisualisierung
- **-website**: Webseite mit mehren Seiten
- **-data**: Sammlung an (Roh-)Daten ohne Skripte
- **-service**: API oder Micro-Service
- **-tool**: Werkzeug, um eine bestimmte Aufgabe zu lösen
- **-guide**: Anleitung, um etwas zu tun

Beispiele für gute Repository-Namen:

- **2019-db-aufzuege-analyse**: Abgeschlossene Analyse der ausgefallenen Aufzüge an Bahnhöfen der Deutschen Bahn.
- **waffenexporte-libyen-analyse**: Laufende Analyse von Waffenexporten nach Libyen.
- **elasticsearch-import-tools**: Mehrere Werkzeuge um Daten in Elasticsearch zu importieren.

## README schreiben

Eine Vorlage für ein typische README-Datei findet sich hier: [README.template.md](https://github.com/digitalegarage/open-source-guidelines/blob/master/README.template.md)

Die Readme-Datei ist die zentrale Quelle für Dokumentation und Informationen über ein Projekt. Ein gut geschriebenes Readme erleichtert den Einstieg in ein Projekt und vermittelt Kompetenz und Ernsthaftigkeit. Im Idealfall umfasst das Readme:  

- **Projekttitel:** Um was geht es bei dem Projekt?
- **Projektbeschreibung:** Welche Funktionen oder Erkenntnisse (bei Analysen) bietet das Projekt? Was macht das Projekt besonders?
- **Demo- oder Artikellink:** Wie sieht das Projekt aus, wenn alles funktioniert? Wie fühlt sich die Benutzeroberfläche an?
- **Datenquelle:** Woher kommen die Daten und wie kann ich sie verwenden (Copyright)?
- **Abhängigkeiten:** Was brauche ich zusätzlich, um das Projekt zum Laufen zu bekommen (z.B. Python 2.7 und PostgreSQL)?
- **Verwendung:** Was muss ich machen, um das Projekt zu verwenden?
- **Funktionen:** Welche Funktionen (oftmals Skripten) hat das Projekt und wie verwende ich diese im Detail?
- **Probleme:** Welche häufigen Probleme gibt es (und wie gehe ich damit um)?
- **Verbesserungen oder Roadmap:** Was kann man besser machen? Wo steht das Projekt und wo soll es mal hin?
- **Dank und Quellen:** Wer hat zum dem Projekt beigetragen, wovon wurde das Projekt inspiriert?

**Wie umfangreich sollte das Readme sein?** In das Readme gehören alle Informationen, die unmittelbar notwendig sind, um das Projekt zu verwenden. Details, wie man eine bestimmte Datenbank aufsetzt, muss man nicht ausführen. Hier reicht ein Link oder zumindest der Hinweis, dass die Installation einer bestimmten Datenbank vorausgesetzt wird (Stichwort Anforderungen).

**Wann sollte ich damit anfangen, ein Readme zu schreiben?** Am besten sofort. Eigentlich sollte man alle Funktionen, die man neu hinzufügt, gleich dokumentieren. Das ist deutlich einfacher, als sich am Ende des Projektes nochmal über alle Funktionen Gedanken machen zu müssen. Außerdem merkt man beim Dokumentieren schnell, ob eine Funktion sinnvoll definiert ist (selbsterklärende Schnittstelle, Abstraktionsniveau).

**Deutsch oder Englisch?** Grundsätzlich empfiehlt sich, alles in Englisch zu dokumentieren. Wenn ein Projekt aber ein ausschließlich deutsches Thema behandelt, kann man aber zumindest die README in Deutsch verfassen. Eine besondere Schwierigkeit ist die Übersetzung von deutschen Behördennamen oder Rechtsbegriffen. Im Fall von *Einspeisevergütung* bespielsweise bietet es sich an, den Originalbegriff und eine Übersetzung zu verwenden: *feed-in tariffs (Einspeisevergütung)*.

Die Dokumentation im Code, sowie Variablen- und Funktionsnamen, sollten eigentlich immer englisch sein. Allerdings gilt auch hier die Ausnahme für Behördennamen und Rechtsbegriffen.

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

Für **Datenanalysen** empfiehlt es sich [Jupyter Notebooks](https://jupyter.org/) oder [R Markdown](http://rmarkdown.rstudio.com/) zu verwenden.

## Commit-Messages

Beim Veröffentlichen des Repositories wird auch der ganze Commit-Verlauf nach außen hin sichtbar. Das sollte eine Motivation sein, sich auch in Zukunft besonders viel Mühe bei den Commit-Messages zu geben. Gute Commit-Messages beginnen mit einem Verb (Imperativ Präsens, erster Buchstabe großgeschrieben) und sind nicht länger als 50 Zeichen. Außerdem braucht man am Ende der Commit-Message keinen Punkt zu setzen.

Beispiel:

```console
$ git commit -m "Fix social media icon alignment in header"
```

## Passwörter entfernen

Manchmal hat man versehentlich Passwörter, API-Keys oder andere vertrauliche Informationen in einem Repo eingecheckt. Diese sollte man unbedingt vor Veröffentlichung des Projektes entfernen. Am einfachsten geht das mit dem [BFG Repo Cleaner](https://rtyley.github.io/bfg-repo-cleaner/). Es empfiehlt sich, das Projekt vorher zu sichern. 

Als erstes muss das Repository gespiegelt werden: 

```console
$ git clone --mirror git@github.com:digitalegarage/mein-repo.git
```

Möglichkeit A: Alle Dateien löschen die *id_rsa* oder *id_dsa* heißen:

```console
$ bfg --delete-files id_{dsa,rsa} mein-repo.git
```

Möglichkeit B: Alle Dateien nach Passwörtern aus einer Liste durchsuchen und mit `***REMOVED***` ersetzen:

```console
$ bfg --replace-text passwords.txt mein-repo.git
```

Um folgende Befehle auszuführen, muss man in das Verzeichnis wechseln:

```console
$ cd mein-repo.git
```

Alle Referenzen aktualisieren und alte Referenzen löschen:

```console
$ git reflog expire --expire=now --all && git gc --prune=now --aggressive
```

Referenzen pushen.

```console
$ git push
```

**Warnung:** Sobald Passwörter in ein öffentliches Repository eingecheckt wurde, sollte man sie als kompromittiert betrachten. In diesem Fall hilft es nur, die betroffenen Passwörter auszutauschen. API-Keys und Auth-Tokens müssen neu generiert werden.

**Vorsorge:** Um zu verhindern, dass sensible Daten eingecheckt werden, sollte man vorsichtig mit globalen Kommandos wie `git add -A` umgehen. Besser ist es, Dateien einzeln zu einem Commit hinzuzufügen. Auf jeden Fall sollten vor einem Commit noch einmal die vorgeschlagenen (staged) Dateien angeschaut werden: `git status`. Um ein versehentliches Einchecken zu verhindern, kann man sensible Konfigurationsdateien auch zur `.gitignore` hinzufügen. Ein .gitignore-Beispiel findet sich in diesem Repository unter `.gitignore`.

## Badges hinzufügen

Sehr beliebt sind sogenannte Badges oder Shields. Sie zeigen bestimmte Projektinformationen, wie die Lizenz, der Build-Status oder die Zahl der Issues, direkt in der README an. Ein vollständige Übersicht findet sich bei [Shields.io](https://shields.io/). Dort kann mit wenigen Klicks Badges für verschiedene Zwecke selbst erzeugen. 

Beispiele aus dem [elasticsearch-frontend](https://github.com/br-data/elasticsearch-frontend):

[![License](https://img.shields.io/github/license/br-data/elasticsearch-frontend.svg?style=flat-square)]() [![GitHub release](https://img.shields.io/github/release/br-data/elasticsearch-frontend.svg?style=flat-square)]() [![GitHub issues](https://img.shields.io/github/issues/br-data/elasticsearch-frontend.svg?style=flat-square)]()

Man sollte sich aber genau überlegen, welche Badges wirklich Sinn machen. Die meisten Informationen sieht man in Github auch so auf einen Blick und mehr als fünf Badges wirken eher unseriös (siehe Heckscheibenaufkleber).

## Lizenz hinzufügen

Damit andere Benutzer den Code für ihre eigenen Projekte nutzen können, braucht das Repository eine Lizenz:

1. Auf der Github-Projektseite **Create new file** auswählen.
2. Als Name der Datei `LICENSE` eingeben.
3. Vorlage **MIT** aus der Liste rechts auswählen.
4. Copyright-Zeile in `Copyright (c) 2017 Bayerischer Rundfunk` ändern.
5. Unten auf der Seite eine Commit-Beschreibung `Add license` eingeben und bestätigen.

**Warnung:** Wichtig ist, dass die Urheberrechte für alle im Repository enthaltene Inhalte (Code, Text, Daten, Schriften, Bilder ...) beim Bayerischen Rundfunk liegen. Fremdinhalte wie Software-Bibliotheken sollten immer über einen Paketmanager – wie beispielsweise [npm](https://www.npmjs.com/), [yarn](https://yarnpkg.com/) oder [pip](https://pypi.python.org/) – installiert werden.

Eine Beispiel-Lizenz (MIT) findet sich in diesem Repository unter `LICENSE`.

## Einstellungen anpassen

Für viele kleinere Projekte ist nicht davon auszugehen, dass sich darum einen Community bilden wird. Die Veröffentlichung dient dabei eher der Transparenz als der Nutzbarmachung. Daher kann man sich überlegen, ob man folgende Optionen in den Projekteinstellungen (Github-Settings > Options) auszuschalten:

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

Wenn man das Repository bereits aus dem eigenen Rechner ausgecheckt hat, muss man den Remote-URL anpassen. Vergisst man die die Remote-URL anzupassen kann man nicht mehr Pushen und Pullen. Die neue URL bekommt man, indem man auf der Github-Projektseite auf **Clone or download** geht. Es empfiehlt sich immer den SSH-Link zu kopieren (statt des HTTPS-Links).

#### In Github Desktop

1. In der rechten oberen Ecke auf *Settings (⚙️) > Repository Settings...* gehen
2. In der Sidebar *Remote* auswählen
3. Im Feld *Primary remote repository* die URL austauschen
4. Mit *Ok* bestätigen und versuchsweise synchronisieren

#### Kommandozeile

Die Remote-URL kann man auch mit folgendem Kommandozeilenbefehl ändern:

```console
$ git remote set-url origin git@github.com:br-data/mein-repo.git
```

Um zu überprüfen, ob die Änderung geklappt hat, kann man sich die Remote-URL mit folgendem Befehl anschauen:

```console
$ git remote -v
origin  git@github.com:br-data/mein-repo.git (fetch)
origin  git@github.com:br-data/mein-repo.git (push)
```

## Gute Beispiele

Gute Beispiele, wie man als Nachrichtenorganisation Daten und Analysen veröffentlichen kann, finden sich bei:

- [SRF Data auf Github](https://github.com/srfdata/)
- [Correctiv! auf Github](https://github.com/correctiv/)

## Kontakt

[BR Data](http://br.de/data/) ist das datenjournalistische Team des [Bayerischen Rundfunks](http://br.de/). Es setzt sich zusammen aus Journalisten, Entwickler und Designern. Wir haben uns auf daten- und dokumentengetriebene Recherche und ihre Umsetzung in interaktiven Anwendungen und im crossmedialen Umfeld spezialisiert.

Wir freuen uns über Fragen, Kritik oder Anregungen:

- BR Data auf Twitter [@br_data](https://twitter.com/br_data/)
- BR Data per [E-Mail](mailto:data@br.de) kontaktieren
