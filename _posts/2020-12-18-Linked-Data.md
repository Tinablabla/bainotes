---
title: "Linked Data"
date: 2020-12-18
---



-- Untertitel --

Heute ist die letzte Vorlesung des BAIN-Kurses dran. Was für eine Reise. Wir haben uns mit vielen Themen befasst und heute wird mit diesem letzten Themenbeitrag einen Schlussstrich gesetzt. Nun ja nicht ganz, _ganz_ am Schluss wird es noch ein Schlussbeitrag geben, der sich mit dem Gelernten auseinandersetzt und einen kleinen Rückblick verschaffen soll.

In dieser letzten Vorlesung soll es um Linked Data gehen. Dabei wurden verschiedene Datenmodelle angesehen: BIBFRAME und RiC, Praxisberichte besprochen und Testumgebungen für Server-Software angeschaut. Ausserdem soll es um Wikidata gehen und Tutorials zum Selberlernen empfohlen werden. RiC wurde bereits in einem [vorherigen Beitrag im Rahmen von Metadaten in Archiven](https://tinablabla.github.io/bainotes/2020/10/09/Metadaten-im-Archiv.html) detailliert angeschaut, weshalb dies hier aussen vor gelassen wird.

## BIBFRAME
BIBFRAME (Bibliographic Framework) ist ein Datenmodell. Wie der Name verrät wird es für bibliografische Daten verwendet und wurde entworfen, um MARC zu ersetzen und das Linked-Data-Prinzip in die Bibliotheken zu bringen. Durch Linked Data soll es möglich sein, der Nutzen von  Bibliothekskataloge zu erhöhen, sowohl innerhalb als auch ausserhalb der Bibliothekscommunity. Das Datenmodell wird seit 2012 auf Initiative der Library of Congress entwickelt. Dabei basiert BIBFRAME auf Functional Requirements of Bibiotgraphic Records (FRBR) und dem Resource Description and Access (RDA), jedoch werden beide nicht vollständig umgesetzt.

#### Das BIBFRAME 2.0 Modell

![BIBFRAME-Modell]({{site.baseurl}}/pictures/BIBFRAME.png)

Das BIBFRAME 2.0 Modell oragnisiert Informationen in drei Abstraktionsebenen: _Work_, _Instance_ und _Item_.
_Work_ ist das höchste Level und beschreibt das grundsätzliche Konzept der Ressource (z.B: Autor, Themen, Sprache). _Instance_ beschreibt Angaben zum Format und dem Verlag. Auf der letzten Stufe wird die Stufe _Item_ aufgeführt, die Angaben zu einem spezifischen Exemplar beinhalten (z.B: Barcode). DIese Aufteilung erscheint sehr sinnvoll, schliesslich kann ein Buch in verschiedenen Verlagen und in verschiedenen Versionen vorhanden sein. Durch dieses Modell kann so die gleiche Entität für den Titel verwendet werden und auf alle verschiedenen Exemplare geschlossen werden.

Oben im Modell definiert das Modell Beziehungen zu anderen Klassen: _Agents_, _Subjects_ und _Events_. _Agents_ beinhaltet alle Personen, die am Werk mitgearbeitet haben, also Autoren/Autorinnen, Editoren/Editorinnen, Cover-Artists, Fotografen/Fotografinnen usw. Da ein Werk mehrere Konzepte vereinen kann, soll _Subjects_ die einzelnen Subjekte aufzeigen: Themen, Orte, Ereignisse, Werke oder Gegenstände. 

### Learnings:
### Quellen:
- [Wikipedia - BIBFRAME](https://de.wikipedia.org/wiki/BIBFRAME)
- [Library of Congress - Overview of the BIBFRAME 2.0 Model](https://www.loc.gov/bibframe/docs/bibframe2-model.html)
