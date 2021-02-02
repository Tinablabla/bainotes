-- Nachtrag zu Metadaten und Einführung in Suchmaschinen --

Da in der letzten Vorlesung viele Themen nicht angesprochen werden konnten, wurden Themen nun in diesen Kurs integriert. Somit starteten wir mit den Nachträgen zu Metadaten. Einerseits gab es eine Diskussion über die Aufgabe der Anreicherung und Erklärungen zu Validierung von XML, Metadatentransformationstools und Nutzung von JSON-APIs sowie dem Metadatenstandard LIDO. Für die Einführung in die Suchmaschinenwurde die Installation und Konfiguration von VuFind vorgenommen und Funktionen von Suchmaschinen am Beispiel von Solr erklärt.

Da im Verlauf des Studiums bereits viel über XML und auch XML Deklarationen erklärt wure, wird in diesem Beitrag nicht darauf eingegangen.

## Vergleich von anderen Datenbearbeitungsprogramme
Neben OpenRefine werden noch andere Tools angesprochen:
- [Catmandu](https://librecat.org)
- [Metafacture](https://github.com/metafacture/metafacture-core)
- [MarcEdit](https://marcedit.reeset.net)

Ich habe aus Interesse, die anderen Tools kurz angeschaut, muss jedoch sagen, dass OpenRefine dank der grafischen Oberfläche viel verständlicher und einfacher zu benutzen ist als beispielsweise Catmandu.
Aus der Präsentation von Prof. Magnus Pfeffer wurde ich noch auf d:swarm aufmerksam. Es sind zwar [Repositories](https://github.com/dswarm) und das [Wiki](https://github.com/dswarm/dswarm-documentation/wiki) zu diesem Tool online, jedoch wurden die seit Ende 2018 nicht mehr weiterentwickelt (gem. GitHub Statistiken) und auch die Webseite <http://www.dswarm.org/> wird auf die [Webseite der Sächsischen Landesbibliothek](https://www.slub-dresden.de/ueber-uns/projekte/juengst-abgeschlossene-projekte/archiv/) umgeleitet. Die Software machte gem. Pfeffer einen guten Eindruck, da ein mächtiges und intuitives Interface versprochen wurde und viele Erweiterungen möglich wären. Leider war es nicht möglich eine Demo auszuprobieren, da auch diese Seite weitergeleitet wurde.

### Quellen:
- [GitHub - d:swarm Wiki](https://github.com/dswarm/dswarm-documentation/wiki)
- Pfeffer, Magnus (2016): Open Source Software zur Verarbeitung und Analyse von Metadaten. Hochschule der Medien.


## Nutzung von JSON-APIs
Bereits in einem [vorletztem Kurs](https://tinablabla.github.io/bainotes/2020/10/30/Metadata-Harvesting.html) haben wir über das Thema Schnittstellen und Metadaten Harvesting gesprochen. Nun wurde dies noch weiter ausgeführt.

Moderne Schnittstellen liefern häufig Antworten in JSON-Format anstatt XML, wie bei SRU oder OAI. JSON steht für JavaScript Object Notation und ist ein kompaktes Datenformat in einer lesbaren Textform. Es dient, wie an den Schnittstellen zu sehen, dem Zweck des Datensaustausches zwischen Anwendungen. Es ist Programmiersprachen unabhängig. Im [letzten Kurs](https://tinablabla.github.io/bainotes/2020/11/20/OpenRefine.html) haben wir Daten aus einer Schnittstelle in das OpenRefine Tool gezogen, welche ebenfalls in JSON formatiert waren.

Zu diesen JSON-APIs wurde eine API und ein Tool vorgestellt. Als API kann [loid-gnd](https://lobid.org/gnd/api) genutzt werden. Ausserdem konnten wir einen Einblick in [scrAPIr](https://scrapir.org) erhalten. Das Tool ermöglicht es, Daten aus Webseiten zu beziehen. Die Webseiten stellen somit eigene APIs zur verfügung und werden mit Hilfe von scrAPIr abgefragt. Da das Tool Vorlagen für den Code in JS und Python zur Verfügung stellt, ist es auch eine nützliche Art einfache Programmierbefehle zu lernen.

Da ich liebend gerne mit solchen Tools herumspiele, habe ich dies natürlich getan. Youtube ist eine meiner grössten Zeitvertreibsünden auf dieser Welt, somit ist klar, dass diese Schnittstelle als erstes getestet wird. Die API setzt den Startpunkt mit dem Suchwort "music" mit 50 Suchergebnissen. Ich habe bereits dazu einigen Gedanken : Nach welcher Relevanz gibt das System die Ergebnisse aus? Youtube (wie Social Media Seiten allgemein) bestehen neben Milliarden von Inhalten vor allem aus Algorithmen, die im Hintergrund so viele Daten verarbeiten, wie sie nur können, um den Nutzenden die "perfekten" Ergebnisse anzuzeigen. So sollen Nutzer länger auf der Plattform bleiben, mehr auf ihr interagieren etc. Eine Schnittstelle greift jedoch nicht als normaler Benutzer zu, sondern als System. Wie entscheidet das System, welche Ergebnisse ausgegeben werden? Man könnte denken, es würden ähnliche Ergebnisse angezeigt werden, wie wenn man mit einem Inkognito Browser darauf zugreift, doch dieser Gedanke trügt. Selbst mit einem Inkognito Browser weiss Google mit welchem Betriebssystem du die Seite aufrufst, was erste Anzeichen auf dein Geschlecht und Alter geben können.

Diese Gedanken wecken meine Neugierde und ich öffne mehrere Fenster:
- Chorome-Fester, mit meinem Login (Spalte: Google Login)
- ein Chrome-Inkognito-Fenster, ohne Login (Spalte: Google Inkognito)
- ein Firefox-Fenster, ohne Login (FirefoWindows)
- ein Firefox-Fenster auf der VM, welche auf Linux läuft, ohne Login (FirefoxLinux)

Somit haben wir den vergleich zwischen verschiedenen Systemen und Browsern. Bei allen Fenstern gebe ich den Suchbegriff "pewdiepie" ein und stelle im Filter als "Typ" nur Videos ein, da auch in der Schnittstelle nur Videos ausgegeben werden.

<table style="width: 923px;">
<tbody>
<tr style="height: 43px;">
<td style="height: 43px; width: 25px;">Nr.</td>
<td style="height: 43px; width: 210px;">Google weiss alles</td>
<td style="height: 43px; width: 210px;">Google weiss fast alles</td>
<td style="height: 43px; width: 210px;">Firefox Windows</td>
<td style="height: 43px; width: 210px;">Firefox Linux</td>
<td style="height: 43px; width: 210px;">scrAPIr</td>
</tr>
<tr style="height: 43px;">
<td style="height: 43px; width: 25px;">1</td>
<td style="height: 43px; width: 210px;">
<p>"This is bad" (PewDiePie)</p>
</td>
<td style="height: 43px; width: 210px;">"This is bad" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"This is bad" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"This is bad" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"This is bad" (PewDiePie)</td>
</tr>
<tr style="height: 43px;">
<td style="height: 43px; width: 25px;">2</td>
<td style="height: 43px; width: 210px;">"Unboxing 100 MIL YouTube AWARD" (PewdDiePie)</td>
<td style="height: 43px; width: 210px;">"Unboxing 100 MIL YouTube AWARD" (PewdDiePie)</td>
<td style="height: 43px; width: 210px;">"Just Another Day In Russia - #79[REDDIT REVIEW]" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"Just Another Day In Russia - #79[REDDIT REVIEW]" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"Conratulations" (PewDiePie)</td>
</tr>
<tr style="height: 43px;">
<td style="height: 43px; width: 25px;">3</td>
<td style="height: 43px; width: 210px;">"was ist mit mir passiert (update video)" (Pocket Hazel)</td>
<td style="height: 43px; width: 210px;">"I Did A DNA Test... (I Guess Im Cancelled Now)" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"Conratulations" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"Conratulations" (PewDiePie)</td>
<td style="height: 43px; width: 210px;">"Uh oh..." (PewDiePie)</td>
</tr>
</tbody>
</table>
