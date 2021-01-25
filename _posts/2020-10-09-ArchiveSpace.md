-- Von Metadatenstandards und dem Archivsystem ArchiveSpace --

In der Vorlesung vom 10. Oktober 2020 wurde sich dem Archivieren gewidmet, genauer gesagt den Metadatenstandards von Archiven und dem ArchiveSpace. Da die Zeit ein wenig knapp berechnet wurde, konnten nicht alle vorgesehenen Punkte dieser Vorlesung abgehandelt werden, so musste zum Beispiel auf zwei Übungen mit ArchiveSpace und die Marktübersicht von Archivsystemen verzichtet werden. Diese wurden in der nächsten Vorlesung behandelt.

In diesem Beitrag wird das Thema Metadatenstandards vertieft. Als erstes wird wiederholt, was ISAD(G) ist und beinhaltet. RiC gewann mein Interesse und soll danach genauer angeschaut und ein kurzes Fazit gezogen werden. Danach wird kurz  ArchiveSpace beschrieben.

## Metadatenstandards

#### ISAD(G)

Im Archiv ist es unglaublich wichtig Archivalien mit Metadaten zu versehen, damit sie auch später wiederverwendet werden können. Die [International Standard Archival Description (General)](https://www.ica.org/en/isadg-general-international-standard-archival-description-second-edition) (kurz ISAD(G)) bildet ein Standard für die Verzeichnung von Archivalien, welcher 1994 entwickelt und 2000 revidiert wurde. Der Standard soll als Leitfaden für archivische Erschliessung und als Instrument zum internationalen Ausstausch dienen. Grundsatz des Standards ist es, nach Provenienzprinzip mit einer mehrstufigen Verzeichnung zu arbeiten.

Die Verzeichnungstufen könenn je nach Grösse des Archivs anders aussehen, grundsätzlich gilt jedoch die hierarchische Abfolge:
- Archiv
- Bestand
- Serie
- Dossier
- Dokument

In ISAD(G) werden 26 Verzeichnungselemente in 7 Informationsbereichen beschrieben:
1. Identifikation
2. Kontext
3. Inhalt und innere Ordnung
4. Zugangs- und Benutzungsbedingungen
5. Sachverwandte Unterlagen
6. Anmerkungen
7. Kontrolle

Ausserdem sind 6 Pflichtfelder von besonderer Bedeutung:
* Signatur
* Titel
* Provenienz
* Entstehungszeitraum
* Umfang
* Verzeichnungsstufe

Der Verband der Schweizerischen Archivarinnen und Archivare (VSA) entwickelte im Jahre 2009 eine [nationale Richtlinie](https://vsa-aas.ch/wp-content/uploads/2015/06/Richtlinien_ISAD_G_VSA_d.pdf), welche die ISAD(G) schweizweit umgesetzt werden soll. Sie berücksichtigt Besonderheiten der schweizerischen Archivlandschaft und deren Regelungsstand im Erschliessungsbereich.

#### Records in Contexts (RiC)
Nach ISAD(G) folgten weitere Standards, welche auf ISAD(G) aufbauten ([ISDF](https://www.ica.org/en/isdf-international-standard-describing-functions), [ISAAR(CPF)](https://www.ica.org/en/isaar-cpf-international-standard-archival-authority-record-corporate-bodies-persons-and-families-2nd), [ISDIAH](https://www.ica.org/en/isdiah-international-standard-describing-institutions-archival-holdings)), jedoch werden diese Standards nicht wirklich von Archvien und Archivsoftwareherstellern übernommen, weshalb ein Neustart erfolgen soll. Records in Contexts (RiC) soll nun alle vorhergehenden Standards ersetzen und aufeinander abstimmen.

Im Jahr 2016 wurde der neue Standardentwurf am Internationalem Archivrat (ICA) am ICA Kongress in Seol vorgestellt. Wie ISAD(G) hält RiC an dem Provenienzprinzip fest und möchte die wichtigsten Entitäten der archivischen Verzeichnung und ihre Eigenschaften dokumentieren. Neu ist jedoch, dass die traditionelle archivische Verzeichnungspraxis nach hierarchischer Form ablegt werden soll. Dies ermöglicht auch parallele und plurale Beziehungen ("sowohl-als-auch"-Beziehungen) zwischen einzelnen Elementen. Traditionelle hierarchische Darstellungen sind durch die RiC weiterhin möglich, da so einfach nur eine Zuweisung zu einer Provenienz vorgenommen wird, RiC bietet jedoch die Möglichkeiten mehrere Provenienzen anzugeben. Mit Hilfe von semantischen Technologien sollen ebenfalls Verknüpfungen von Metadaten zwischen verschiedenen Institutionen (beispielsweise Archive und Bibliotheken) ermöglicht werden. Dies ist im Sinne der Linked Open Data, was erst in der letzten Vorlesung vom 18. Dezember 2020 besprochen wird.

RiC besteht aus drei Teilen:
1. RiC-CM -- abstraktes Konzeptmodell
2. [RiC-O](https://ica-egad.github.io/RiC-O/) -- Formale und technische Repräsentation des Modells als Ontologie
3. RiC-AG -- Application Guidelines für Softwareentwickler

RiC befindet sich noch in der Entwurfphase. Es ist jedoch eine Verabschiedung der Version 1.0 Ende 2020 geplant, welche jedoch aufgrund der COVID-19-Pandemie in Verzug geraten könnte. Geplant ist, die ersten beiden Teile des RiC in der Version 1.0 zu veröffentlichen und danach den dritten Teil zu erarbeiten. Seit März 2020 ist die [Source der Ontologie (RiC-O)](https://github.com/ICA-EGAD/RiC-O) auf GitHub aufrufbar.

#### Fazit
ISAD(G) wurde zu einer Zeit entwickelt, in der die Digitalisierung erst begann und deshalb auch im Standard nicht weiter beachtet wurde. RiC wirkt dahingehend vielversprechend und zukunftsorientiert. Es macht Sinn, Metadaten zu verknüpfen und allen Gedächnisinstitutionen zugänglich zu machen. Jedoch fällt bei den Recherchen auf, dass die Entwicklung des Standards sehr undurchsichtig ist. Die mangelnde Transparenz wurde auch von InterPARES Trust als Kritik angebracht. Da es sich jedoch um eine Weiterentwicklung der bestehenden Standards handelt, wird ein kompletter Paradigmenwechsel ausbleiben und vertraute Muster wiederkehren. Dadurch, dass auch Baum-Hierarchien in RiC abgebildet werden können, sollte eine Überführung in der Theorie einfach möglich sein. Wie die technsichen Lösungen dazu aussehen, werden wir in den nächsten Jahren erfahren. 

### Learnings:
- ISAD(G) ist der Standard für die Verzeichnung von Archivalien
- Wichtige Aspekte des Standards sind die Verzeichnungsstufen, Verzeichnungselemente und das Provenienzprinzip
- In der Schweiz wurde eine Richtlinie zur Umsetzung des Standards erarbeitet
- RiC soll alle bisherigen Standards ersetzen und zusammenführen
-

### Quellen:
- [Schweizerische Richtlinie für die Umsetzung von ISAD(G)](https://vsa-aas.ch/wp-content/uploads/2015/06/Richtlinien_ISAD_G_VSA_d.pdf)
- [ISAD(G): Internationale Grundsätze für die archivische Verzeichnung](https://www.ica.org/sites/default/files/CBPS_2000_Guidelines_ISAD%28G%29_Second-edition_DE.pdf)
- [Webinar VSA AG Normen und Standards, 1.7.2020: Mehrdimensionale Erschliessung mit
Records in Contexts (RiC)](https://wiki.docuteam.ch/lib/exe/fetch.php?media=docuteam:praes_vsa-ric_20200701_wildi.pdf)
-[ogdan Florin Popovici: “Records in Contexts – Towards a New Level in Archival Description?”](http://www.pokarh-mb.si/uploaded/datoteke/Radenci/radenci_2016/013-031_popovici_2016.pdf)



Zwischenstand:

## ArchiveSpace





















### Learnings:
-
-

### Quellen:
-
-
