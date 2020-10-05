-- titel --

Heute starteten wir mit ein paar Kommentaren und Ergänzungen der Dozenten zu den Lerntagebüchern, konnten eine Pullrequest mit Git machen, lernten den Unterschied zwischen MARC21 und Dublin Core und installierten mehr oder weniger erfolgreich Koha. Als erstes möchte ich zuerst über mein heutiges Vertiefungsthema reden, bevor ich auf die restlichen Punkte eingehe. 

## Git und Github

Wir wissen, dass Github Repositories statische Webseiten erstellt werden können. Diese Webseite ist mit Github erstellt und liegt in einem Repository. Mittels Jekyll werden die Markup- und HTML-Dateien intepretiert und als Webseite angezeigt. 
Git ist eine Versionenkontrollsoftware, sie macht genau das, sie kontrolliert Versionen und vergleicht sie miteinander. Dies ermöglicht dem Benutzer die Wiederherstellung einer älteren Version. Git wird lokal auf dem Rechner installiert, ist gratis und ist einfach zu bedienen. Eine Besonderheit von Git ist das Branching Model, dass dir erlaubt eine Kopie des aktuellen Codes zu machen und innerhalb des Branches neue Ideen auszuprobieren ohne den originalen Code kapput zu machen. 

Github hingegen ist ein Git repository hosting serice, eine online Datenbank, welche dir die Möglichkeit gibt, die Git-Projekte und die verschiedenen Versionen deines Projekts zu teilen. Github ist ausschliesslich cloud based und kann zwar in der Basisversion gratis genutzt werden, bietet jedoch zahlreiche Lizenzmodelle an. Vor allem unter Open-Source Projekten ist Github sehr beliebt. Mir bekannte Projekte, welche auf Github geteilt werden, sind beispielsweise die [offizielle deutsche Corona-Warn-App](https://github.com/corona-warn-app) oder [das open source Bibliothektsprogramm Koha](https://github.com/Koha-Community/Koha) auf welches wir im nächsten Blogpost noch genauer eingehen werden. Auch in Github ist es möglich Branches zu erstellen und diese wieder zu vereinen mittels Push/Pull-Requests. Wenn also Git ein Gesicht ist, ist Github Facebook. 

Im Rahmen der Vorlesung konnten wir eine Pull-Request an Herrn Lohmeier stellen.  Die Installation von Git war erfolgreich, jedoch war ich unfähig den Texteditor zu benutzen. Zuerst fehlten mir die Rechte, welche ich mir glücklicherweise selbst vergeben konnte, danach kam jedoch der Editor ins Spiel, welcher mir anfangs Kopfschmerzen bereitet hatte. Dank [dieser Webseite](http://www.linuxandubuntu.com/home/how-to-use-vi-editor#:~:text=vi%20is%20a%20screen%2Doriented,Ubuntu%2C%20Linux%20Mint%20or%20Debian) fand ich mich dann doch noch zurecht und konnte die Request doch noch machen. 



Inhalt der Vorlesung
- Kommentare zu Lerntagebüchern
  CodiMD wird zu HedgeDoc, Jekyll, Bilder (rechte beachten, in neuen Ordner einfügen)
- Versionskontrolle mit Git
  Git nicht auf VM, Git installiert, dann Editor nicht händeln können, https://de.wikipedia.org/wiki/Chmod und http://www.linuxandubuntu.com/home/how-to-use-vi-editor#:~:text=vi%20is%20a%20screen%2Doriented,Ubuntu%2C%20Linux%20Mint%20or%20Debian. sei dank, hat es dann doch funktioniert.
  Carprentry lesson ist empfehlenswert, git wird nicht weiter verwendet, aber kann für das lerntagebuch verwendet werden. Konnte schlussentlich eine Pull Request machen.
- Funktion und Aufbau von Bibliothekssystemen 1/2 
  - Metadatenstandards in Bibliotheken (MARC21)
    Unterschied MARC21/DC
  - Installation und Konfiguration von Koha
    Funktioniert bis zur aufrufung der Webseite http://bibliothek-intra.meine-schule.org/, da komme ich nicht weiter. Notfalls mit Demo arbeiten. Dozent geht dem Problem nach. 
  - Aufgabe
