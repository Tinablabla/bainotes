-- Metataden ernten und VuFindHarvest --

Im Kurs wurde das Thema Schnittstellen mehrmals angesprochen, jedoch möchten wir heute genau klären, was es damit auf sich hat.

## Schnittstellen und Metadaten Harvesting

- [Z39.50](https://de.wikipedia.org/wiki/Z39.50) (Library of Congress)
- [SRU](https://de.wikipedia.org/wiki/Search/Retrieve_via_URL) - Search/Retrieve via URL (Library of Congress)
- [OAI-PMH](https://de.wikipedia.org/wiki/Open_Archives_Initiative) - Open Archives Initiative Protocol for Metadata Harvesting (Open Archives Initiative)


Die drei aufgeführten Punkte sind alles bekannte und weit verbreitete Übertragungsprotokolle im Bibliotheks- und Archivwesen. Z39.50 ist die älteste Variante und wurde 1984 in den USA entwickelt. Diese Schnittstelle wird zwar noch benutzt, ist jedoch veraltet. SRU basiert auf den etablierten Internet-Standards wie URI und XML und ist im Gegensatz zu Z39.50 auch über das Bibliothekswesen hinaus bekannt. Sie kam im Rahmen einer Initiative, Z39.50 International Next Generation (ZING), zustande und soll eine Weiterentwicklung der Z39.50-Schnittstelle werden.

Heute werden wir hauptsächlich mit der AOI-Schnittstelle arbeiten und haben bereits in anderen Vorlesungen mit ihr gearbeitet. Das [OAI-PMH](http://www.openarchives.org/OAI/openarchivesprotocol.html) wurde 2000 entwickelt, da Publikationen häufig verstreut über Server verschiedener Institutionen gesucht werden müssen. Während Z39.50 verschiedene Anfragen an mehrere Hosts stellen muss, sammelt OAI-PMH einfach die bereitgestellten Daten von Data Providern. Data Provider können beispielsweise Repositories (siehe dazu mein letzter Beitrag [Repository Software](https://tinablabla.github.io/bainotes/2020/10/16/Repository-Software.html)) sein, die eine AOI-Schnittstelle zulassen. Die gesammelten Datensätze werden von Service Providern (wie [BASE](https://de.wikipedia.org/wiki/Bielefeld_Academic_Search_Engine), die mit Solr/Lucene betrieben wird) für Suchanfragen aufbereitet. Da es viele Metadatenformate gibt (mehr dazu auch im Beitrag [Metadaten im Archiv](https://tinablabla.github.io/bainotes/2020/10/09/Metadaten-im-Archiv.html)) wird das Dublin Core Datenmodell vorgeschrieben.

Dieser Sammelvorgang von Daten heisst auch Metadata Harvesting. Der Begriff Metadata Harvesting beschreibt also das Sammeln von Metadaten von verschiedenen Data Providern und das Speichern auf einer zentralen Datenbank. In der Vorlesung verwenden wir dazu VuFindHarvest.

### Learnings:
- Es gibt drei bekannte Schnittstellen: Z39.50, SRU, OAI-PMH
- OAI-PMH sammelt in Repositories Daten ein und werden von Service Providern aufbereitet (Metadaten Harvesting)

### Quellen:
- [Wikipedia -- Search/Retrieve via URL](https://de.wikipedia.org/wiki/Search/Retrieve_via_URL)
- [Wikipedia -- Open Archives Initiative](https://de.wikipedia.org/wiki/Open_Archives_Initiative)
- [UCF Libraries -- Metadata Harvesting](https://guides.ucf.edu/metadata/metaHarvesting)

## VuFindHarvest
VuFindHarvest ist eine Open Source Software (Code auf [GitHub](https://github.com/vufind-org/vufindharvest)), die für das sammeln von Metadaten entwickelt wurde. Dabei kann das Tol eine Datei pro Datensatz oder mehrere Dateien pro Datensatz verarbeiten. Die Datensätze können durch Konfigurationen erweitert und bearbeitet werden. Interessant finde ich, dass die Software in einer .txt Datei das Datum der letzten "Ernte" speichert, damit später eine schrittweise Aktualisierung und das Abrufen neuer Inhalte möglich ist. Ausserde werden auch abgebrochene Prozesse abgespeichert und können fast nahtlos weitergeführt werden.

VuFindHarvest ist im Rahmen des [VuFind](https://vufind.org/vufind/) Projektes entstanden. VuFind ist ein Open Source Discorvery-System, welches den Online Public Access Catalogue (OPAC) ablösen kann. Auf der Webseite des Projekts gibt es eine [Tabelle](https://vufind.org/wiki/community:installations) mit Organisationen, welche mit dem Tool arbeiten. Unter anderem werden [swissbib](https://www.swissbib.ch/) (welche per 31. März 2021 eingestellt wird und durch SLSP ersetzt wird), [META-Katalog](https://www.meta-katalog.eu/) (zentrale Suche für über 30 Frauen- und Lesebnarchiven und Bibliotheken), [BASE](https://www.base-search.net/) (Bielefeld Academic Search Engine) und Bibliotheken von den Universitäten [Chemnitz](https://www.tu-chemnitz.de/ub/), [Darmstadt](https://www.ulb.tu-darmstadt.de/service/start/index.en.jsp) und [Hamburg](https://www.tub.tuhh.de/).

In der Vorlesung haben wir VuFindHarvest genutzt, um die Metadaten von Koha (in MARC21-XML), ArchivesSpace (in EAD) und DSpace (Dublin Core) zu sammeln und auf der Festplatte gespeichert. Um die Daten zu vereinheitlichen wurden sie danach in einem XSLT Crosswalk auf das Format MARC21-XML konvertiert.

## Quellen:
- [GitHub -- VuFindHarvest](https://github.com/vufind-org/vufindharvest)
- [VuFind -- About](https://vufind.org/vufind/about.html)

Zeichen: 3637
