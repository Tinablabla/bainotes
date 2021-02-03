---
title: "Einführung in Bibliothekssysteme"
date: 2020-09-25
---


-- Versionenkontrollen, Metadatenstandards in Bibliotheken und die Installation von Koha --

Heute starteten wir mit ein paar Kommentaren und Ergänzungen der Dozenten zu den Lerntagebüchern, installierten und verwendeten Git, lernten den Unterschied zwischen MARC21 und Dublin Core und installierten mehr oder weniger erfolgreich Koha. Als erstes möchte ich zuerst über mein heutiges Vertiefungsthema reden, bevor ich auf die restlichen Punkte eingehe.

## Git und GitHub
Wir wissen, dass mit GitHub Repositories statische Webseiten erstellt werden können. Diese Webseite ist mit GitHub erstellt und liegt in einem solchen Repository. Mittels Jekyll werden die Markup- und HTML-Dateien inteprretiert und als Webseite angezeigt.

Git ist eine Versionenkontrollsoftware und wie der Name sagt, kontrolliert sie Versionen und vergleicht sie miteinander. Dies ermöglicht dem Benutzer die Wiederherstellung einer älteren Version. Git wird lokal auf dem Rechner installiert, ist gratis und einfach zu bedienen. Eine Besonderheit von Git ist das Branching Modell, dass dir erlaubt eine Kopie des aktuellen Codes zu machen und innerhalb des Branches neue Ideen auszuprobieren ohne den originalen Code zu beschädigen.

GitHub hingegen ist ein Git Repository Hosting Service, eine online Datenbank, welche dir die Möglichkeit gibt, die Git-Projekte und die verschiedenen Versionen deines Projekts zu teilen. GitHub ist ausschliesslich cloud based und kann zwar in der Basisversion gratis genutzt werden, bietet jedoch zahlreiche Lizenzmodelle an. Vor allem unter Open Source Projekten ist GitHub sehr beliebt. Mir bekannte Projekte, welche auf GitHub geteilt werden, sind beispielsweise die [offizielle deutsche Corona-Warn-App](https://GitHub.com/corona-warn-app) oder [das Open Source Bibliothektsprogramm Koha](https://GitHub.com/Koha-Community/Koha) auf welches wir im [nächsten Blogpost](https://tinablabla.github.io/bainotes/2020/10/02/Koha.html) noch genauer eingehen werden. Auch in GitHub ist es möglich Branches zu erstellen und diese wieder zu vereinen mittels Push/Pull-Requests. Wenn also Git ein Gesicht ist, ist GitHub Facebook.

Im Rahmen der Vorlesung konnten wir eine Pull-Request an Herrn Lohmeier stellen.  Die Installation von Git war erfolgreich, jedoch hatte ich schwierigkeiten mit dem Texteditor. Dank [dieser Webseite](http://www.linuxandubuntu.com/home/how-to-use-vi-editor#:~:text=vi%20is%20a%20screen%2Doriented,Ubuntu%2C%20Linux%20Mint%20or%20Debian) fand ich mich dann doch noch zurecht und konnte die Request doch noch machen.

Auch wenn es unwahrscheinlich ist, dass ich jemals ein Programm schreibe, möchte ich GitHub im Hinterkopf behalten. Ich könnte mir vorstellen GitHub wieder als Blog zu nutzen, da mir Markup gefällt und die Versionenkontrolle für einen gemeinsamen Blog nützlich sein könnte. Ein weiterer Nutzen könnte vielleicht ein gemeinsames Learning-Repository sein, in welchem eine ganze Klasse ihre Notizen und Skripts eintragen und Zusammenfassungen gemeinsam erstellen können. So könnten auch spätere Generationen von Informationswissenschaftlern auf diese Dateien zugreifen.

### Learnings:
- Git ist eine offline Versionenkontrollsoftware, GitHub ist die online-cloud Version von Git.
- GitHub wird vor allem für Open-Source-Projekte verwendet.
- Pull-Request selbst machen

### Quellen:
- [Devmountain - Git vs. GitHub: What's the Difference?](https://blog.devmountain.com/git-vs-GitHub-whats-the-difference/)

### Nachtrag
Nur einen Tag nachdem ich diesen Beitrag geschrieben habe, sind mein Partner und ich auf die Idee gekommen, einen Rezept-Manager zu benutzen. Damit wollen wir eine Sammlung von Rezepten erstellen, welche wir selbst einmal gekocht haben und gut funktionieren. Nun war ich ein bisschen in den Weiten des Internets unterwegs und fand heraus, dass einige Programme auf GitHub existieren und gratis von GitHub gehostet werden können. Ein Beispiel, dass mir zumindest optisch gefällt, wäre [Chowdown](https://chowdown.io/). Ich werde sicher dran bleiben und versuchen, das Ganze selbst hinzubekommen. Jetzt nachträglich bin ich sehr froh, haben wir in einem anderen Kurs Python gelernt und hier nun eine Einführung in GitHub erhalten. So eröffnet sich für uns nicht nur beruflich sondern auch privat ganz neue Türen. Ausserdem: wenn man etwas aus intrinsischer Motivation nebenbei lernt (z.B: Programmieren während dem Rezepte eintragen), lernt man viel schneller. Somit, en guetä! Jetzt muss ich nurnoch sicherstellen, dass das Essen nicht kalt wird :).

## MARC21 und Dublin Core
Bei der Übung zum Vergleich der beiden Standards wurde uns anschaulich gezeigt, was die Unterschiede zwischen MARC21 und Dublin Core sind. MARC21 kam dabei, meiner Meinung nach, eher schlecht weg. Es wirkte unübersichtlich und voll von nicht interpretierbaren Codes. Während DC viel schlanker wirkte, waren auch die unterschiedlichen Werke klar voneinander trennbar.
Im Gegenzug ist es in MARC21 möglich, spezifische Codes einzusetzten, um Elemente genauer zu beschreiben. DC kennt beispielsweise nur einen Code für Contributor, wohingegen MARC21 gleich sechs Codes kennt, welche alle in unterschiedlicher Weise genutzt werden.

### Learnings:
- DC einfacher zu lernen als MARC21
- MARC21 beschreibt genauer als DC
- Im XML Format ist DC einfacher lesbar als MARC21

### Quellen:
- [DOCPLAYER - Compaison of Dublin Core and MARC/MARC21](https://docplayer.net/37045281-Comparison-of-dublin-core-and-marc-marc21.html)

## Koha
Zum Schluss konnten wir bereits Vorbereitungen für die nächste Vorlesung treffen, indem wir das Open Source Bibliotheksprogramm Koha installieren und konfigurieren konnten. Leider funktionierte auch dies nicht problemlos. Irgendwo hatte ich eine Zeile UNIX Shell Befehle vergessen, was zu einer fehlerhaften Installation führte. Herr Lohmeier wird dem Problem nachgehen.

Zeichen: 4207(Ohne Nachtrag)
