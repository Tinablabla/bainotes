-- Versionenkontrollen, Metadatenstandarts und die Installation von Koha --

Heute starteten wir mit ein paar Kommentaren und Ergänzungen der Dozenten zu den Lerntagebüchern, installierten und verwendeten Git, lernten den Unterschied zwischen MARC21 und Dublin Core und installierten mehr oder weniger erfolgreich Koha. Als erstes möchte ich zuerst über mein heutiges Vertiefungsthema reden, bevor ich auf die restlichen Punkte eingehe. 

## Git und Github
Wir wissen, dass Github Repositories statische Webseiten erstellt werden können. Diese Webseite ist mit Github erstellt und liegt in einem Repository. Mittels Jekyll werden die Markup- und HTML-Dateien intepretiert und als Webseite angezeigt. 
Git ist eine Versionenkontrollsoftware, sie macht genau das, sie kontrolliert Versionen und vergleicht sie miteinander. Dies ermöglicht dem Benutzer die Wiederherstellung einer älteren Version. Git wird lokal auf dem Rechner installiert, ist gratis und ist einfach zu bedienen. Eine Besonderheit von Git ist das Branching Model, dass dir erlaubt eine Kopie des aktuellen Codes zu machen und innerhalb des Branches neue Ideen auszuprobieren ohne den originalen Code kapput zu machen. 

Github hingegen ist ein Git repository hosting serice, eine online Datenbank, welche dir die Möglichkeit gibt, die Git-Projekte und die verschiedenen Versionen deines Projekts zu teilen. Github ist ausschliesslich cloud based und kann zwar in der Basisversion gratis genutzt werden, bietet jedoch zahlreiche Lizenzmodelle an. Vor allem unter Open-Source Projekten ist Github sehr beliebt. Mir bekannte Projekte, welche auf Github geteilt werden, sind beispielsweise die [offizielle deutsche Corona-Warn-App](https://github.com/corona-warn-app) oder [das open source Bibliothektsprogramm Koha](https://github.com/Koha-Community/Koha) auf welches wir im nächsten Blogpost noch genauer eingehen werden. Auch in Github ist es möglich Branches zu erstellen und diese wieder zu vereinen mittels Push/Pull-Requests. Wenn also Git ein Gesicht ist, ist Github Facebook. 

Im Rahmen der Vorlesung konnten wir eine Pull-Request an Herrn Lohmeier stellen.  Die Installation von Git war erfolgreich, jedoch war ich unfähig den Texteditor zu benutzen. Zuerst fehlten mir die Rechte, welche ich mir glücklicherweise selbst vergeben konnte, danach kam jedoch der Editor ins Spiel, welcher mir anfangs Kopfschmerzen bereitet hatte. Dank [dieser Webseite](http://www.linuxandubuntu.com/home/how-to-use-vi-editor#:~:text=vi%20is%20a%20screen%2Doriented,Ubuntu%2C%20Linux%20Mint%20or%20Debian) fand ich mich dann doch noch zurecht und konnte die Request doch noch machen. 

Auch wenn es unwahrscheindlich ist, dass ich jemals ein Programm schreibe, möchte ich Github im Hinterkopf behalten. Ich könnte mir vorstellen Github wieder als Blog zu nutzen, da mir Markup gefällt und die Versionenkontrolle für einen gemeinsamen Blog nützlich sein könnte. Ein weiterer Nutzen könnte vielleicht ein gemeinsames Learning-Repository sein, in welchem eine ganze Klasse ihre Notizen und Skripts eintragen und Zusammenfassungen gemeinsam erstellen können. So könnten auch spätere Generationen von Informationswissenschaftlern auf diese Dateien zugreifen. 

### Learnings:
- Git ist eine offline Versionenkontrollsoftware, Github ist die online-cloud Version von Git.
- Github ist vor allem für Open-Source-Projekte verwendet.
- Pull-Request selbst machen

### Quellen:
- <https://blog.devmountain.com/git-vs-github-whats-the-difference/>

### Nachtrag
Nur einen Tag nachdem ich diesen Beitrag geschrieben habe, sind mein Partner und ich auf die Idee gekommen, einen Rezept-Manager zu benutzen. Damit wollen wir eine Sammlung von Rezepten erstellen, welche wir selbst einmal gekocht haben und gut funktionierten. Nun war ich ein bisschen in den Weiten des Internets unterwegs und fand heraus, dass einige Programme auf Github existieren und gratis von Github gehostet werden können. Ein Beispiel, dass mir zumindest optisch gefällt, wäre [Chowdown](https://chowdown.io/). Ich werde sicher dran bleiben und zusehen, dass ich das Ganze selbst hinbekomme. Jetzt nachträglich bin ich sehr froh haben wir Python gelernt und eine Einführung in Github erhalten haben. So eröffnet sich für uns nicht nur beruflich sondern auch privat ganz neue Türen. Ausserdem: wenn man etwas aus intrinsischer Motivation nebenbei lernt (z.B: Programmieren während dem Rezepte eintragen), lernt man viel schneller. Somit, en guetä! Jetzt muss ich nurnoch zusehen, dass das Essen nicht kalt wird :).

## MARC21 und Dublin Core
Bei der Übung zum Vergleich von den beiden Standards wurde uns anschaulich gezeigt, was die Unterschiede zwischen MARC21 und Dublin Core sind. MARC21 kam dabei, meiner Meinung nach, eher schlecht weg. Es wirkte unübersichtlich und voll von nicht intepretierbarer Codes. Während DC viel schlanker wirkte, waren auch die unterschiedlichen Werke klar voneinander trennbar. 
Dafür ist es in MARC21 möglich, spezifische Codes einzusetzten, um Elemente genauer zu beschreiben. DC kennt beispielsweise nur einen Code für Contributor, wo MARC gleich sechs Codes kennt, welche alle in unterschiedlicher Weise genutzt werden.

### Learnings:
- DC einfacher zu lernen
- MARC21 beschreibt genauer
- Im XML Format ist DC einfacher lesbar

### Quellen: 
- <https://docplayer.net/37045281-Comparison-of-dublin-core-and-marc-marc21.html>

## Koha
Zum Schluss konnten wir bereits vorbereitungen für die nächste Vorlesung treffen, indem wir das open-source Bibliotheksprogramm Koha installieren und konfigurieren konnten. Leider funktionierte auch dies nicht problemlos. Irgendwo hatte ich eine Zeile UNIX Shell Befehle vergessen, was zu einer fehlerhaften Installation führte. Herr Lohmeier wird dem Problem nachgehen. 

### Learnings:
- nochmals genau kontrollieren, welche Codes bereits drin sind und welche nicht.
