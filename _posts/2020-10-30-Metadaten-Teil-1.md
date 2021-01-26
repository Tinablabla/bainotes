-- Untertitel --

Im Kurs wurde das Thema Schnittstellen mehrmals bereits angesprochen, jedoch möchten wir heute genau klären, was es damit auf sich hat.

## Metadaten

#### Schnittstellen und Metadaten Harvesting

- [Z39.50](https://de.wikipedia.org/wiki/Z39.50) (Library of Congress)
- [SRU](https://de.wikipedia.org/wiki/Search/Retrieve_via_URL) - Search/Retrieve via URL (Library of Congress)
- [OAI-PMH](https://de.wikipedia.org/wiki/Open_Archives_Initiative) - Open Archives Initiative Protocol for Metadata Harvesting (Open Archives Initiative)
Die drei aufgeführten Punkte sind alles bekannte und weit verbreitete Übertragungsprotokolle im Bibliotheks- und Archivwesen. Z39.50 ist die älteste Variante und wurde 1984 in den USA entwickelt. Diese Schnittstelle wird zwar noch benutzt, ist jedoch veraltet. SRU basiert auf den etablierten Internet-Standards wie URI und XML und ist im Gegensatz zu Z39.50 auch über das Bibliothekswesen hinaus bekannt. Sie kam im Rahmen einer Initiative, Z39.50 International Next Generation (ZING), zustande und soll eine Weiterentwicklung der Z39.50-Schnittstelle werden.
Heute werden wir hauptsächlich mit der AOI-Schnittstelle arbeiten und haben bereits in anderen Modulen mit ihr gearbeitet. Das OAI-PMH wurde 2000 entwickelt, da Publikationen häufig verstreut über Server verschiedener Institutionen gesucht werden müssen. Während Z39.50 verschiedene Anfragen an mehrere Hosts stellen muss, sammelt OAI-PMH einfach die bereitgestellten Daten von Data Providern. Die gesammelten Datensätze werden von Service Providern für Suchanfragen aufbereitet. Da es viele Metadatenformate gibt (mehr dazu auch im Beitrag [Metadaten im Archiv](2020-10-09-Metadaten im-Archiv.md))

## Quellen:
- [Wikipedia -- Search/Retrieve via URL](https://de.wikipedia.org/wiki/Search/Retrieve_via_URL)
- [Wikipedia -- Open Archives Initiative](https://de.wikipedia.org/wiki/Open_Archives_Initiative)
