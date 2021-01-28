-- Untertitel --

In der heutigen Vorlesung wurde der zweite Teil der Metadaten und Schnittstellen Thematik angesprochen. Dabei wurde OpenRefine erklärt und verwendet, ausserdem werden Fragen zu den Library Carpentry Lessons geklärt und eine Übung zu CSV nach MARC21-XML mit OpenRefine gelöst. Für diese Vorlesung mussten Aufgaben gelöst werden, da diese die Grundlagen für den Kurs bieten. In diesem Beitrag werden die gewonnenen Erkentnisse aus den Hausaufgaben und dem Unterricht vermischt. Ausserdem wollte ich für diesen Beitrag vermehrt meine Erfahrungen mit den Hausaufgaben aufzeigen.

## OpenRefine

Auf der offiziellen [Website](https://openrefine.org/) wird das Tool folgendermassen beschrieben:

>OpenRefine (previously Google Refine) is a powerful tool for working with messy data: cleaning it; transforming it from one format into another; and extending it with web services and external data.

Ausserdem werden die im Zitat aufgeführte verendungszwecke nochmals genauer beschrieben:

**1. Explore Data**

Das Tool bietet veschiedene Möglichkeiten Daten anzusehen und zu sortieren. Öffentlich zugängliche Daten sind oft nicht uniform, was dazu führt, dass beispielsweise ähnliche Datensätze aus zwei ähnlichen Institutionen kommen, jedoch andere Namen für die selben Begriffe verwenden. Dies führt dazu, dass es zu Inkonsistenzen kommt. Um dies zu vereinheitlichen, bietet OpenRefine ein Facet/Filter-Tab, in dem alle Inhalte einer Spalte o.a. aufgezählt werden und mit wenigen Klicks Inkonsistenzen aufgeklärt werden können. Wichtig zu wissen: Es werden alle Bearbeitungsschritte verfolgt und im Undo/Redo-Tab können diese Bearbeitungen rückgängig gemacht oder wiederholt werden. Ausserdem ist es möglich diese Schritte zu exportieren und in einem anderen Datenset zu wiederholen (ähnlich wie Aktionen in Photoshop).

**2. Clean and Transform Data**

Daten können in verschiedenen Formen auftreten. Manchmal hat man eine Liste, möchte jedoch eine Tabelle. Mit OpenRefine ist es möglich mit verschiedenen Commands und Funktionen solche Tabellen zu erstellen und Daten zu transformieren.

**3. Rconcile and Match Data**

Mit Hilfe von Webservices ist es möglich, die eigenen Daten zu verlinken und zu erweitern. Einer davon ist Wikidata.


Für die Software git es verschiedene [Dokumentationen](https://openrefine.org/documentation.html), die den Usern und Entwikcklern helfen können. Ausserdem gibt es eine [Library Carpentry Lesson](https://librarycarpentry.org/lc-open-refine/) zu OpenRefine, welche wir als Hausaufgabe lösten.

## Carpentry Lesson: OpenRefine

Disclaimer: Mit diesem Kapitel möchte ich etwas anderes ausprobieren. Ich werde die Hausaufgabe lösen und währenddessen ein AHA-Sheet ausfüllen, jedoch in elektronischer Form. Ein AHA-Sheet ist (nach meiner Interpretation und Verständnis) ein Blatt Papier, dass während des Lernens mit AHA Momenten oder wichtigen Fakten ausgefüllt wird. Dies soll den Lerneffekt verstärken, was dazu führt, dass das Gelernte länger im Kopf bleibt. Ausserdem hilft es in der Zukunft: Wenn man ein Thema nochmals anschaut und sich das AHA-Sheet zur Hilfe nimmt, sieht man alles was man gelernt hat auf einen Blick. Somit: Geht schneller rein, bleibt länger drin und falls es doch noch weg gehen sollte, hat man etwas, dass das Gelernte zurückholt. Das Sheet muss es nicht sonderlich strukturiert sein, ist es jedoch bei mir fast immer. Da ich sowieso dieses AHA-Sheet mache, möchte ich dies als mein Beitrag festhalten. Da ich mich hierbei nicht auf Zeichenanzahl begrenzen möchte, bitte ich um Verständnis, falls dieser Beitrag länger wird als gedacht. Jedoch interessiert mich dieses Tool sehr, da das Arbeiten mit Daten eine Leidenschaft von mir ist. Ich bin nur noch nicht sonderlich gut darin :) aber an dem lässt sich Arbeiten!

#### Aufgabe 2
Importierbare Datafiles:
- TSV (tab-separated values)
- CSV (comma-separated values)
- Excel
- JSON (javascript object notation)
- XML
- Google Spreadsheet

- "Trim leading and trailing whitespace from strings[...]" führt bei einer checked Box dazu, dass wenn Leerschläge das letzte Zeichen eines Feldes sind, die Leerschläge ignoriert werden. So wird ein English_ zu English hinzugezählt.

#### Aufgabe 3
- Zellen teilen: Spalte auswählen -> `Edit cells` -> `Split multi-valued cells`
- Zellen vereinen: Spalte auswählen -> `Edit cells` -> `Join multi-valued cells`
- Unterschied `Records` und `Rows`: Rows zählt die einzelnen Reihen, während Records zusammengehörige Reihen verlinkt und nur die Records aufzählt.
- Gute Trennzeichen zeichenen sich durch ihre Einzigartigkeit aus, `|` ist sehr beliebt, `,` ist meist ungeeignet, da es häufig vorkommt. Kommt jedoch auf die Daten an und wie sie aufgeteilt werden sollen.

#### Aufgabe 4
- Für jede Spalte kann ein Facet erstellt werden
- Es gibt verschiedene Arten von Facets (Text, Numerische, Timeline, Streudiagramm und Benutzerdefinierte)
- Es können eigene erstellt werden, aber es gibt auch `Customized facets`
- Textfilter funktioniert wie Excel Suche

#### Aufgabe 5
- Clustering bedeutet gleiche aber inkonsistente Angaben zu vereinen, nützlich bei Variationen von Abkürzungen und ausgeschriebenen Namen ect.
- Key Collision funktioniert bei gleichen Zeichen aber es fehlen Zeichen oder sind zusätzliche Zeichen vorhanden oder in einer anderen Reihenfolge.
- Nearest Neighbor zeigt wenn einzelne Buchstaben nicht stimmen (G. Anbalagan / K. Anbalagan), jedoch kann ich hier nicht sicher sein, ob dies korrigiert werden muss. Es gibt schliesslich genug Personen mit den gleichen Nachnamen, die Bücher und Artikel veröffentlichen.


#### Aufgabe 7 & 8
- Transformations findet man unter: `Edit cells -> Transform...`
-  [GREL](https://github.com/OpenRefine/OpenRefine/wiki/General-Refine-Expression-Language) (General Refine Expression Language) ist eine vereinfachte und effiziente Sprache zur Bearbeitung von Daten und hat Ähnlichkeiten zu Excel Formeln, jedoch liegt der Fokus von GREL auf Text und nicht auf Nummern.
- GREL kennt zwei Schreibarten:
    - value.function(options)
    - function(value, options)
- `Help` gibt eine Liste von GREL Funktionen aus und wie sie genutzt werden können.

#### Aufgabe 10














Zeichen:
