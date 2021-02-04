---
title: "JSON-Schnittstellen"
date: 2020-11-27
---


-- Ein abschweifendes Youtube-Experiment mit Hilfe von Schnittstellen --

Da in der letzten Vorlesung viele Themen nicht angesprochen werden konnten, wurden Themen nun in diesen Kurs integriert. Somit starteten wir mit den Nachträgen zu Metadaten. Einerseits gab es eine Diskussion über die Aufgabe der Anreicherung und Erklärungen zu Validierung von XML, Metadatentransformationstools und Nutzung von JSON-APIs sowie dem Metadatenstandard LIDO. Für die Einführung in die Suchmaschinen wurde die Installation und Konfiguration von VuFind vorgenommen und Funktionen von Suchmaschinen am Beispiel von Solr erklärt.

Da im Verlauf des Studiums bereits viel über XML und auch XML Deklarationen erklärt wurde, wird in diesem Beitrag nicht darauf eingegangen. Ausserdem ist der Teil zu JSON-APIs ein wenig ausführlich ausgefallen, deshalb wird das Suchmaschinenthema für den [nächsten Beitrag](https://tinablabla.github.io/bainotes/2020/12/11/VuFind-&-Solr.html) aufgehoben.

## Vergleich von anderen Datenbearbeitungsprogrammen
Neben OpenRefine werden noch andere Tools angesprochen:
- [Catmandu](https://librecat.org)
- [Metafacture](https://github.com/metafacture/metafacture-core)
- [MarcEdit](https://marcedit.reeset.net)

Ich habe aus Interesse, die anderen Tools kurz angeschaut, muss jedoch sagen, dass OpenRefine dank der grafischen Oberfläche viel verständlicher und einfacher zu benutzen ist als beispielsweise Catmandu.
Aus der Präsentation von Prof. Magnus Pfeffer wurde ich noch auf d:swarm aufmerksam. Es sind zwar [Repositories](https://github.com/dswarm) und ein [Wiki](https://github.com/dswarm/dswarm-documentation/wiki) zu diesem Tool online, jedoch wurden diese seit Ende 2018 nicht mehr weiterentwickelt (gem. GitHub Statistiken) und auch die Webseite <http://www.dswarm.org/> wird auf die [Webseite der Sächsischen Landesbibliothek](https://www.slub-dresden.de/ueber-uns/projekte/juengst-abgeschlossene-projekte/archiv/) umgeleitet. Die Software machte gem. Pfeffer einen guten Eindruck, da ein mächtiges und intuitives Interface versprochen wurde und viele Erweiterungen möglich wären. Leider war es nicht möglich eine Demo auszuprobieren, da auch diese Seite weitergeleitet wurde.

### Quellen:
- [GitHub - d:swarm Wiki](https://github.com/dswarm/dswarm-documentation/wiki)
- Pfeffer, Magnus (2016): Open Source Software zur Verarbeitung und Analyse von Metadaten. Hochschule der Medien.


## Nutzung von JSON-APIs
Bereits im [vorletztem Kurs](https://tinablabla.github.io/bainotes/2020/10/30/Metadata-Harvesting.html) haben wir über das Thema Schnittstellen und Metadaten Harvesting gesprochen. Nun wurde dies noch weiter ausgeführt.

Moderne Schnittstellen liefern häufig Antworten in JSON-Format anstatt XML, wie bei SRU oder OAI. JSON steht für JavaScript Object Notation und ist ein kompaktes Datenformat in einer lesbaren Textform. Es dient, wie an den Schnittstellen zu sehen, dem Zweck des Datenaustausches zwischen Anwendungen. Es ist Programmiersprachen unabhängig. Im [letzten Kurs](https://tinablabla.github.io/bainotes/2020/11/20/OpenRefine.html) haben wir Daten aus einer Schnittstelle in das OpenRefine Tool gezogen, welche ebenfalls in JSON formatiert waren.

Zu diesen JSON-APIs wurde eine API und ein Tool vorgestellt. Als API kann [loid-gnd](https://lobid.org/gnd/api) genutzt werden. Ausserdem konnten wir einen Einblick in [scrAPIr](https://scrapir.org) erhalten. Das Tool ermöglicht es, Daten aus Webseiten zu beziehen. Die Webseiten stellen somit eigene APIs zur Verfügung und werden mit Hilfe von scrAPIr abgefragt. Da das Tool Vorlagen für den Code in JS und Python zur Verfügung stellt, ist es auch eine nützliche Art einfache Programmierbefehle zu lernen.

Da ich liebend gerne mit solchen Tools herumspiele, habe ich dies natürlich getan. Youtube ist eine meiner grössten Zeitvertreibsünden, somit ist klar, dass diese Schnittstelle als erstes getestet wird. Die API setzt den Startpunkt mit dem Suchwort "music" mit 50 Suchergebnissen. Ich habe dazu bereits einige Gedanken: Nach welcher Relevanz gibt das System die Ergebnisse aus? Youtube (wie Social Media Seiten allgemein) bestehen neben Milliarden von Inhalten vor allem aus Algorithmen, die im Hintergrund so viele Daten verarbeiten, wie sie nur können, um den Nutzenden die "perfekten" Ergebnisse anzuzeigen. So sollen Nutzer länger auf der Plattform bleiben, mehr auf ihr interagieren etc. Eine Schnittstelle greift jedoch nicht als normaler Benutzer zu, sondern als System. Wie entscheidet das System, welche Ergebnisse ausgegeben werden? Man könnte denken, es würden ähnliche Ergebnisse angezeigt werden, wie wenn man mit einem Inkognito Browser darauf zugreift, doch dieser Gedanke trügt. Selbst mit einem Inkognito Browser weiss Google mit welchem Betriebssystem du die Seite aufrufst, was erste Anzeichen auf dein Geschlecht und Alter geben können.

Diese Gedanken wecken meine Neugierde und ich öffne Youtube in mehreren Fenstern:
- ein Chrome-Fester, mit meinem Login (Spalte: Chrome Login)
- ein Chrome-Inkognito-Fenster, ohne Login (Spalte: Chrome Inkognito)
- ein Firefox-Fenster, ohne Login (Firefox Windows)
- ein Firefox-Fenster auf der VM, welche auf Linux läuft, ohne Login (Firefox Linux)

Somit haben wir den Vergleich zwischen verschiedenen Systemen, Browsern und der Abfrage von scrAPIr. Bei allen Fenstern gebe ich den Suchbegriff "pewdiepie" ein und stelle im Filter "Typ" nur Videos ein, da auch in der Schnittstelle nur Videos ausgegeben werden. Zur Erstellung der Tabelle wurde die Weibseite <https://divtable.com/converter/> verwendet.


<table style="width: 923px;">
<tbody>
<tr style="height: 43px;">
<td style="height: 43px; width: 25px;">Nr.</td>
<td style="height: 43px; width: 210px;">Chrome&nbsp;Login</td>
<td style="height: 43px; width: 210px;">Chrome&nbsp;Inkognito</td>
<td style="height: 43px; width: 210px;">Firefox Windows</td>
<td style="height: 43px; width: 210px;">Firefox Linux</td>
<td style="height: 43px; width: 210px;">scrAPIr</td>
</tr>
<tr style="height: 43px;">
<td style="height: 43px; width: 25px;">1</td>
<td style="height: 43px; width: 210px;">"This is bad" (PewDiePie)</td>
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

Es ist interessant zu sehen, dass zumindest das erste Video bei allen Abfragen das selbe Ergebnis ergibt. Chrome möchte anscheinend, dass ich mir das Unboxig Video ansehe, hingegen schlägt mir Firefox ein Reddit Review vor, egal auf welchem Betriebssystem ich mich befinde. scrAPIr zieht als zweites Video jedoch das Musikvideo "Congratulations" vor, welches zumindest bei Firefox an dritter Stelle angezeigt wird. Chrome kann sich für den dritten Platz nicht entscheiden und gibt mir mit Login die Empfehlung einer deutschen Youtuberin an, von welcher ich in den letzten 6 Monaten kein Video mehr gesehen habe. Im Inkognito wird mir wieder ein PewDiePie Video vorgeschlagen, welches sonst nirgends unter den ersten drei zu finden ist. Dasselbe gilt für scrAPIr: Auch dort wird auf dem Dritten Platz ein anderes Video vorgeschlagen als "üblich".

#### Fazit
Dieser Vergleich zeigt, wie unterschiedlich die Empfehlungen von Youtube sein können. Es überrascht jedoch, dass die selben Ergebnisse für unterschiedliche Betriebssysteme angezeigt werden, somit könnte daraus geschlossen werden, dass der Algorithmus den Browser als Angabe bevorzugt. Ebenfalls ist es interessant zu sehen wie unterschiedlich die Ergebnisse mit und ohne Login sind: Sie unterscheiden sich auf Chrome nur auf dem dritten Platz, jedoch wird mit Login ein Video einer deutschen Youtuberin bevorzugt, obwohl ich seit längerem kein Video mehr von ihr gesehen habe aber regelmässig Videos von PewDiePie anschaue. Ich könnte mir das Ergebnis so erklären, dass der Algorithmus Videos mit viel Interaktion (Likes, Views, Kommentaren) in der Auflistung bevorzugt und dadurch das neuste Video als erstes angegeben wird. Als zweites wird auf den Browser geachtet, denn diese Ergebnisse sind deckungsgleich. Der dritte Vorschlag erinnert bei der Chrome-mit-Login-Suche an eine normale Videoempfehlung aus der Startseite, unabhängig vom Suchbegriff. Da diese Empfehlung bei anderen Browsern fehlt, werden weitere PewDiePie Videos angezeigt. Selbstverständlich ist dieser Versuch keineswegs repräsentativ, aber es ist unglaublich faszinierend zu sehen, was die Unterschiede der Systeme sind. Die Frage bleibt jedoch: Wie und warum werden die Ergebnise für die Schnittstelle ausgewählt?


Ich bin ein wenig vom Thema abgeschweift. Ich habe neben der Youtube-Schnittstelle auch noch Reddit ausprobiert, was auch gut funktionierte. Gerade mit der aktuellen [Gamestop-Aktien-Situation](https://www.nzz.ch/finanzen/flashmob-an-der-boerse-wie-kleinanleger-hedge-funds-jagen-und-kurse-in-die-hoehe-treiben-ld.1599017) wäre es spannend ein Python-Programm zu schreiben, um die Posts aus dem Subreddit [Wallstreetbets](https://www.reddit.com/r/wallstreetbets/) zu analysieren. Vielleicht finde ich während den Semesterferien die Zeit dazu :)

Zeichen: 7152 (ohne Tabelle)
