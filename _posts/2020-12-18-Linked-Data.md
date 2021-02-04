---
title: "BIBFRAME"
date: 2020-12-18
---



-- ein Linked Data Datenmodell --

Heute ist die letzte Vorlesung des BAIN-Kurses. Was für eine Reise. Wir haben uns mit vielen Themen befasst und heute wird mit diesem letzten Themenbeitrag einen Schlussstrich gesetzt. Nun ja nicht ganz, _ganz_ am Schluss wird es noch ein Schlussbeitrag geben, der sich mit dem Gelernten auseinandersetzt und einen kleinen Rückblick verschaffen soll.

In dieser letzten Vorlesung soll es um Linked Data gehen. Dabei wurden verschiedene Datenmodelle angesehen, BIBFRAME und RiC, und Praxisberichte besprochen. RiC wurde bereits in einem [vorherigen Beitrag im Rahmen von Metadaten in Archiven](https://tinablabla.github.io/bainotes/2020/10/09/Metadaten-im-Archiv.html) detailliert angeschaut, weshalb dies hier aussen vor gelassen wird.

## BIBFRAME
[BIBFRAME](https://www.loc.gov/bibframe/) (Bibliographic Framework) ist ein Datenmodell. Wie der Name verrät, wird es für bibliografische Daten verwendet und wurde entworfen, um MARC zu ersetzen und das Linked-Data-Prinzip in die Bibliotheken zu bringen. Durch Linked Data soll es möglich sein, den Nutzen von  Bibliothekskatalogen zu erhöhen, sowohl innerhalb als auch ausserhalb der Bibliothekscommunity. Das Datenmodell wird seit 2012 auf Initiative der Library of Congress entwickelt. Dabei basiert BIBFRAME auf Functional Requirements of Bibiotgraphic Records (FRBR) und dem Resource Description and Access (RDA), jedoch werden beide nicht vollständig umgesetzt.

#### Das BIBFRAME 2.0 Modell

![BIBFRAME-Modell]({{site.baseurl}}/pictures/BIBFRAME.png)

Das BIBFRAME 2.0 Modell organisiert Informationen in drei Abstraktionsebenen: _Work_, _Instance_ und _Item_.
_Work_ ist das höchste Level und beschreibt das grundsätzliche Konzept der Ressource (z.B: Autor:in, Themen, Sprache). _Instance_ beschreibt Angaben zum Format und Verlag. Auf der letzten Ebene wird die Stufe _Item_ aufgeführt, die Angaben zu einem spezifischen Exemplar beinhalten (z.B: Barcode). Diese Aufteilung erscheint sehr sinnvoll, schliesslich kann ein Buch in verschiedenen Verlagen und in verschiedenen Versionen vorhanden sein. Durch dieses Modell kann so die gleiche Entität für den Titel verwendet werden und auf alle verschiedenen Exemplare geschlossen werden.

Das Modell definiert zusätzlich Beziehungen zu anderen Klassen: _Agents_, _Subjects_ und _Events_. _Agents_ beinhaltet alle Personen, die am Werk mitgearbeitet haben, also Autoren/Autorinnen, Editoren/Editorinnen, Cover-Artists, Fotografen/Fotografinnen usw. Da ein Werk mehrere Konzepte vereinen kann, soll _Subjects_ die einzelnen Subjekte aufzeigen: Themen, Orte, Ereignisse, Werke oder Gegenstände die im Werk behandelt werden. Die (für mich persönlich) am schwersten greifbare Klasse ist _Events_. Auf der Webseite von [Library of Congress](https://www.loc.gov/bibframe/docs/bibframe2-model.html) wird es folgendermassen erklärt: "
>Occurrences, the recording of which may be the content of a Work.

In der Vorlesung wird ein Beispiel mit einem Theaterstück genannt, welches die Klasse _Event_ sehr gut erklärt:
>Wenn man eine Aufzeichung eines Theaterstücks hat, dann ist das Theaterstück das Event, denn es ist der Inhalt des Werks nicht das Thema des Werks.

Somit ist BIBFRAME eine Ontologie für Bibliotheksressourcen, welche ähnliche "Felder" aufweist wie MARC, doch durch Linked Data einen neuen Ansatz und vielleicht auch eine andere Philosophie in die Bibliothekswelt bringt.


### Learnings:
- BIBFRAME ist ein Linked Data Datenmodell für bibliographische Daten
- basiert auf aktuellen Standards, setzt sie jedoch nicht ganz um
- Unterteilt zwischen einer Werk-, Instanz- und Exemplarebene und hat unterschiedliche Klassen für die Personen, die mit dem Werk involviert sind, Subjekte die im Werk vorkommen und Events, die Aufzeichnungen von anderen Inhalten besser bezeichnen lässt.

### Quellen:
- [Wikipedia - BIBFRAME](https://de.wikipedia.org/wiki/BIBFRAME)
- [Library of Congress - Overview of the BIBFRAME 2.0 Model](https://www.loc.gov/bibframe/docs/bibframe2-model.html)

Zeichen: 3530
