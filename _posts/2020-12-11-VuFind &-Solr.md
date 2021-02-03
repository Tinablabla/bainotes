---
title: "VuFind & Solr"
date: 2020-12-11
---



-- Suchmaschinen und Discovery-Systeme--

In diesem Beitrag möchte ich die Themen vom letzten und dem heutigen Kurs angehen und aus diesem Grund wird der heutige Eintrag über Suchmaschinen und Discovery-Systeme handeln. Wir werden VuFind installieren und konfigurieren und FUnktionen von Suchmaschinen anschauen. Ausserdem gab es in der Vorlesung eine Übung zu Datenintegration und eine Gruppendiskussion zum perfekten Katalog. Zum Schluss wird eine Marktübersicht von Discovery-Systemen behandelt.

## Unterschied Discovery-System und Suchmaschine
Wichtig anzumerken ist der Unteschied zwischen Discovery-Systemen und Suchmaschinen:

[Wikipedia-Artikel zu Suchmaschine](https://de.wikipedia.org/wiki/Suchmaschine)
>Eine Suchmaschine ist ein Programm zur Recherche von Dokumenten, die in einem Computer oder einem Computernetzwerk wie z. B. dem World Wide Web gespeichert sind. Nach Erstellung einer Suchanfrage, oftmals durch Texteingabe eines Suchbegriffs, liefert eine Suchmaschine eine Liste von Verweisen auf möglicherweise relevante Dokumente, meistens dargestellt mit Titel und einem kurzen Auszug des jeweiligen Dokuments. Dabei können verschiedene Suchverfahren Anwendung finden.

Hauptaufgaben einer Suchmaschine sind:
- Index erstellen und pflegen
- Suchanfragen bearbeiten
- Sinnvolle Aufbereitung der Suchergebnissen

Beispiele für Suchmaschinen sind Google, Bing und Solr.

[Wikipedia-Artikel zu Discovery-System](https://de.wikipedia.org/wiki/Suchmaschine)
>Discovery-Systeme sind bibliothekarische Suchsysteme, die auf Suchmaschinentechnologie beruhen. Die sind Bestandteil des Konzepts der Bibliothek 2.0 und sollen die bisherigen OPAC-Kataloge ergänzen oder gar ersetzen.

Somit ist ein Discovery-System eine Art Suchmaschinem jedoch sich die Begriffe nicht gleich zu setzten. Ein Beispiel für ein Discovery-System ist VuFind.

## VuFind
Wir hatten bereits eine Begegnung mit VuFind in der [Metadata Harvesting Lektion](https://tinablabla.github.io/bainotes/2020/10/30/Metadata-Harvesting.html). Dort haben wir mit dem VuFindHarvest Tool gearbeitet, um Metadaten zu "ernten". VuFind ist eine Open Source Software, die ein Portal für Bibliotheksressourcen ist. Den Benutzern soll das Suchen und das Browsen durch die Ressourcen vereinfachen und den traditionellen OPAC ersetzen. Es soll Katalogdatensätze, Bibliotheksobjekte, Repositories und eine Bibliographie vereinen. Der Sourcecode ist auf [GitHub](https://github.com/vufind-org/vufind) zu finden.


## Solr
Die Open Source Suchplattform Solr gilt als "Industriestandard". Das Discovery-System von VuFind basiert ebenfalls auf Solr, jedoch ist das nur eines von vielen Beispielen. Auf der [offiziellen Webseite von Solr](https://lucene.apache.org/solr/) wird die Suchplattform als hochgradig zuverlässig, skalierbar und fehlertolerant beschrieben.
Es gibt eine ausführliche [Dokumentation](https://lucene.apache.org/solr/guide/8_8/) und ein [Wiki](https://cwiki.apache.org/confluence/display/solr). Im Wiki ist auf der Seite [PublicServers](https://cwiki.apache.org/confluence/display/solr/PublicServers) eine Übersicht zu sehen, auf welchen Seiten Solr genutzt wird. Interessante Beispiele sind Netflix, Disney, NASA, Instagram und eBay.

#### Learings:
- Discovery-Systeme sind nicht mit Suchmaschinen gleichzusetzen
- VuFind ist ein Discovery-System und basiert auf Solr
- Solr ist eine Suchmaschine und gilt als Industriestandard

#### Quellen:
- [VuFind - About](https://vufind.org/vufind/about.html)
- [Wikipedia - Apache Solr](https://en.wikipedia.org/wiki/Apache_Solr)
- [Solr](https://lucene.apache.org/solr/)
