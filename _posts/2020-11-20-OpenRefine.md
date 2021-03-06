---
title: "OpenRefine"
date: 2020-11-20
---

-- "a powerful tool for working with messy data" --

In der heutigen Vorlesung wurde der zweite Teil der Metadaten und Schnittstellen Thematik angesprochen. Dabei wurde OpenRefine erklärt und verwendet, ausserdem werden Fragen zu den Library Carpentry Lessons geklärt und eine Übung zu CSV nach MARC21-XML mit OpenRefine gelöst. Für diese Vorlesung mussten Aufgaben gelöst werden, da diese die Grundlagen für den Kurs bieten. In diesem Beitrag werden die gewonnenen Erkenntnisse aus den Hausaufgaben und dem Unterricht vermischt. Das Hauptthema in diesem Beitrag wird OpenRefine und die Carpentry Lesson dazu sein.

Disclaimer: Mit diesem Beitrag möchte ich etwas anderes ausprobieren. Ich werde die Hausaufgabe lösen und währenddessen ein AHA-Sheet machen, jedoch in elektronischer Form. Ein AHA-Sheet ist (nach meiner Interpretation und Verständnis) ein Blatt Papier, dass während des Lernens mit AHA-Momenten oder wichtigen Fakten ausgefüllt wird. Dies soll den Lerneffekt verstärken, was dazu führt, dass das Gelernte länger im Kopf bleibt. Ausserdem hilft es in der Zukunft: Wenn man ein Thema nochmals anschaut und sich das AHA-Sheet zur Hilfe nimmt, sieht man alles, was man gelernt hat, auf einen Blick. Somit: Geht schneller rein, bleibt länger drin und falls es doch noch weg gehen sollte, hat man etwas, dass das Gelernte zurückholt. Das Sheet muss nicht sonderlich strukturiert sein, ist es jedoch bei mir fast immer. Da ich sowieso ein AHA-Sheet mache, möchte ich dies in diesem Beitrag festhalten. Da ich mich hierbei nicht auf eine Zeichenanzahl begrenzen möchte, bitte ich um Verständnis, falls dieser Beitrag länger wird als gedacht.

## Einführung

Auf der offiziellen [Website](https://openrefine.org/) wird das Tool folgendermassen beschrieben:

>OpenRefine (previously Google Refine) is a powerful tool for working with messy data: cleaning it; transforming it from one format into another; and extending it with web services and external data.

Ausserdem werden die im Zitat aufgeführten Verwendungszwecke nochmals genauer beschrieben:

**1. Explore Data**

Das Tool bietet veschiedene Möglichkeiten, Daten anzusehen und zu sortieren. Öffentlich zugängliche Daten sind oft nicht uniform, was dazu führt, dass beispielsweise ähnliche Datensätze aus zwei ähnlichen Institutionen kommen, jedoch andere Namen für die selben Begriffe verwenden. Dies führt zu Inkonsistenzen im Datensatz. Um dies zu vereinheitlichen, bietet OpenRefine ein Facet/Filter-Tab, in dem alle Inhalte einer Spalte o.a. aufgezählt werden und mit wenigen Klicks Inkonsistenzen aufgeklärt werden können. Wichtig zu wissen: Es werden alle Bearbeitungsschritte verfolgt und im Undo/Redo-Tab können diese Bearbeitungen rückgängig gemacht oder wiederholt werden. Ausserdem ist es möglich diese Schritte zu exportieren und in einem anderen Datenset zu wiederholen (ähnlich wie Aktionen in Photoshop).

**2. Clean and Transform Data**

Daten können in verschiedenen Formen auftreten. Manchmal hat man eine Liste, möchte jedoch eine Tabelle. Mit OpenRefine ist es möglich mit verschiedenen Commands und Funktionen solche Tabellen zu erstellen und Daten zu transformieren.

**3. Reconcile and Match Data**

Mit Hilfe von Webservices ist es möglich, die eigenen Daten zu verlinken und zu erweitern. Einer davon ist Wikidata.


Für die Software git es verschiedene [Dokumentationen](https://openrefine.org/documentation.html), die den Usern und Entwicklern helfen können. Ausserdem gibt es eine [Library Carpentry Lesson](https://librarycarpentry.org/lc-open-refine/) zu OpenRefine, welche wir als Hausaufgabe lösten.

## Carpentry Lesson: OpenRefine
Nachdem wir nun die Grundlagen über das Tool erfahren haben, wenden wir uns nun der Lesson zu. Zu jeder Aufgabe, bei der ich etwas wichtiges lerne oder erfahre, werde ich hier den AHA-Moment festhalten.

#### Aufgabe 2
- "Trim leading and trailing whitespace from strings[...]" führt bei einer checked Box dazu, dass wenn Leerschläge das letzte Zeichen eines Feldes sind, die Leerschläge ignoriert werden. So wird ein English_ zu English hinzugezählt.

Importierbare Datafiles:
  - TSV (tab-separated values)
  - CSV (comma-separated values)
  - Excel
  - JSON (javascript object notation)
  - XML
  - Google Spreadsheet



#### Aufgabe 3
- Zellen teilen: Spalte auswählen -> `Edit cells` -> `Split multi-valued cells`
- Zellen vereinen: Spalte auswählen -> `Edit cells` -> `Join multi-valued cells`
- Unterschied `Records` und `Rows`: Rows zählt die einzelnen Reihen, während Records zusammengehörige Reihen verlinkt und nur die Records aufzählt.
- Gute Trennzeichen zeichnen sich durch ihre Einzigartigkeit aus, `|` ist sehr beliebt, `,` ist meist ungeeignet, da es häufig vorkommt. Kommt jedoch auf die Daten an und wie sie aufgeteilt werden sollen.

#### Aufgabe 4
- Für jede Spalte kann ein Facet erstellt werden
- Es gibt verschiedene Arten von Facets (Text, Numerische, Timeline, Streudiagramm und Benutzerdefinierte)
- Es können eigene erstellt werden, aber es gibt auch `Customized facets`
- Textfilter funktioniert wie Excel Suche

#### Aufgabe 5
- Clustering bedeutet gleiche aber inkonsistente Angaben zu vereinen, nützlich bei Variationen von Abkürzungen und ausgeschriebenen Namen ect.
- Key Collision funktioniert bei gleichen Zeichen aber es fehlen Zeichen oder sind zusätzliche Zeichen vorhanden oder in einer anderen Reihenfolge.
- Nearest Neighbor zeigt, wenn einzelne Buchstaben nicht stimmen (G. Anbalagan / K. Anbalagan), jedoch kann ich hier nicht sicher sein, ob dies korrigiert werden muss. Es gibt schliesslich genug Personen mit den gleichen Nachnamen, die Bücher und Artikel veröffentlichen.


#### Aufgabe 7 & 8
- Transformations findet man unter: `Edit cells -> Transform...`
-  [GREL](https://github.com/OpenRefine/OpenRefine/wiki/General-Refine-Expression-Language) (General Refine Expression Language) ist eine vereinfachte und effiziente Sprache zur Bearbeitung von Daten und hat Ähnlichkeiten zu Excel Formeln, jedoch liegt der Fokus von GREL auf Text und nicht auf Nummern.
- GREL kennt zwei Schreibarten:
  - value.function(options)
  - function(value, options)
- `Help` gibt eine Liste von GREL Funktionen aus und wie sie genutzt werden können.
- gesammelte GREL Funktionen:
  - `value.toTitlecase()` -- Nur Der Erste Buchstabe Gross
  - `value.toUppercase()` -- CAPSLOCK MODE ACTIVATED
  - `value.toLowercase()` -- capslock mode deactivated
  - `value.toDate("dd/MM/yyyy")` -- gibt Datum als im Date-Format aus (01/11/2020)
  - `value.toString("dd MMMM yyyy")` -- gibt Datum in String aus (1 November 2020)
  - `value.contains("test")` -- prüft, ob "test" vorkommt, je nach Ergebnis `true/false`
  - `if(value.contains("test"),"Test data",value)` -- prüft ob "test" vorkommt, wenn `true` wird der Zelleninhalt durch "Test data" ersetzt
  - `value.split(",")` -- macht eine kommagetrennte String-Liste in eine Arry
  - `value.split(",").sort()` -- ^ + alphabetisch sortiert
  - `value.split(",").sort().join(",")` -- ^ + ^ + fügt sie wieder zu einem String zusammen.
  - `value.split(",")[0]` -- ^ + extrahiert eine spezifische Variable (hier die Erste, da 0 der Startpunkt ist)
  - `value.match(/(.*),(.*)/)` -- Input ist eine regular Expression und es wird ein Array ausgegeben, bei denen die regular Expression zutrifft. `/`signalisieren die regular Expression, `()` signalisieren, dass eine Gruppe von Zeichen verglichen wird, `.*` signalisiert, dass irgend ein Zeichen garnicht, einmal oder mehrmals vorkommt. Somit wird verglichen: Hat es eine Zelle, die (ein oder mehrere oder kein) Buchstabe(n), gefolgt von einem `,` und (einem, mehreren oder keinem) Buchstaben enthält? -> Wenn etwas gefunden wird, wird die Zelle in einen Array transfomiert.
- `value.match(/(.*),(.*)/).reverse().join(" ")` -- Macht die Funktion von ^ rückängig und fügt alles in einen String.

#### Aufgabe 10
- Jedes Stück Daten hat ein `type`. OpenRefine kennt die folgenden Datentypen:
  - String ("Beispielname")
  - Number ("12345")
  - Date ("20/02/2020")
  - Boolean ("true/false")
  - Array ([“Monday”,”Tuesday”,”Wednesday”,”Thursday”,”Friday”,”Saturday”,”Sunday”])

#### Aufgabe 11
- Arrays sind Listen in eckigen `[]` Klammern von Daten, die mit Hilfe von Anführungs- und Schlusszeichen `"` und Kommas `,` getrennt werden. Sie können einfacher bearbeitet werden als andere Listen in einem Datenblatt.

#### Aufgabe 12
- Export in verschiede Formate möglich:
  - HTML
  - Excel
  - csv
  - tsv
  - ODF

#### Aufgabe 13
- Stars and Flags können zur Kennzeichning von Reihen dienen, unter `All` können nach den beiden Zeichen sortiert werden.

#### Aufgabe 14
HOLY SHIT IT WORKED!

<img src="https://media.giphy.com/media/VvXg0yjJQgfEQ/giphy.gif" width="300" />

- Looking up data from a URL: Spalte erstellt auf ISSN mit `Add column by fetching URLs`, Klick auf `Show`, bei "User-Agent" `; mailto:address@library.edu` (mit eigenen Angaben) hinzugeben, GREL-Feld: `"https://api.crossref.org/journals/"+value`, dies bedeutet, dass mit Hilfe dieses API zu dieser ISSN Daten in JSON gezogen werden konnten. OpenRefine hat eine Funktion `value.parseJson()`, die Daten aus JSON extrahieren kann.

- Reconciliation services  und Extensions habe ich nicht ausprobiert.

## Fazit

Dieses Tool ist mir unglaublich sympatisch. Mit ein wenig Einführung kann man schon unglaublich nützliche Befehle lernen und die Daten sind schon nach kurzer Zeit bearbeitet. Die Carpentry Lesson zeigt eigentlich das, was in den Introduction-Videos von OpenRefine gezeigt wird, jedoch viel einfacher erklärt. Es fasziniert mich, wie viel aus der Software herausgeholt werden kann und wie nahtlos die verschiedenen Schnittstellen arbeiten. Ich kann mir gut vorstellen auch in Zukunft damit zu arbeiten.

Zeichen:


![too many to count](https://media.giphy.com/media/ejfQbLsh2rFfi/giphy.gif)
