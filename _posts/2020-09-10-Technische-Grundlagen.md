---
title: "Technische Grundlagen"
date: 2020-09-10
---


-- Was ich über Markdown lernte und wie meine VM versagte --

Da in der ersten Vorlesung auch viele Formalitäten geklärt werden müssen, konnten wir nur grundlegende Themen behandeln. Nach einer ausführlichen Vorstellungsrunde lernten wir [CodiMD](https://pad.gwdg.de/) kennen, welches zur Formatierung [Markdown](https://www.markdownguide.org/basic-syntax/) vewendet, konnten unseren Zugriff auf eine für uns persönlich eingerichtete Virtuelle Maschine (VM) beziehen und die VM auch gleich austesten, indem wir verschiedene Unix Shell Übungen bearbeiten konnten.

## Markdown
Markdown ist eine vereinfachte Auszeichnungssprache, die es ermöglicht, durch gängige Symbole, einfache Formatierungen darzustellen. Sie ist besonders einfach durch den Menschen lesbar und anwendbar. Dies lässt sich an einer Gegebüberstellung von HTML, welche ebenfalls eine Auszeichnungssprache ist, und Markdown besonders einfach zeigen:

In HTML kann ein Text mit dem Tag `<strong>`oder `<b>` fettgedruckt werden.
<p>Der Hund heisst <b>Bello</b></p>

    <p>Der Hund heisst <b>Bello</b></p>

In Markdown kann das gleiche Ergebnis mit zwei Asterisken am Anfang und Ende erreicht werden:

Der Hund heisst **Bello**

    Der Hund heisst **Bello**

An diesem Beispiel ist einfach zu erkennen, dass das Öffnen und Schliessen der Tags in HTML viel mehr Aufwand bereitet, als das Einsetzen von zwei zusätzlichen Zeichen vor und nach dem Wort.


In der Praxis kann Markdown in verschiedenen Situationen angewendet werden: Reddit ist eine Webseite, auf welcher Benutzer in verschiedenen Foren Inhalte hochladen, teilen und diskutieren können. Diese Beiträge können (wenn gewünscht) mit Markdown formatiert werden. Auch dieser Lerntagebucheintrag ist mit Markdown geschrieben, denn auch Github Pages verwendet Markdown. Ein weiteres Beispiel ist CodiMD, welches bald zu HedgeDoc umbenennt wird.

Der Einführungsartikel ist für mich zur Zeit noch ein kleiner Spielplatz für verschiedene Markdown-Befehle. Ich habe mich lange mit der Tabelle herumgeschlagen. Dabei habe ich herausgefunden, dass viele Tags aus dem HTML übertragen werden können, da Github Pages das einbinden von HTML Tags unterstützt. So konnte ich zuerst die Tabelle in HTML auszeichnen, bevor ich es dann doch mit ein wenig probieren in Markdown geschafft habe. Da ich schon unbewusst mit Markdown gearbeitet habe, war es für mich ein Leichtes, im gemeinsamen Dokument und auch hier auf dem Blog damit zu arbeiten. Die Auszeichnungssprache erscheint mir sinnvoll und sehr einfach zu lernen. Bis anhin gab es auf den Seiten und Applikationen die ich verwende eine Guidepage ([Github](https://guides.github.com/features/mastering-markdown/), [Reddit](https://www.reddit.com/wiki/markdown), [Discord](https://support.discord.com/hc/de/articles/210298617-Markdown-Text-101-Chat-Formatierung-Fett-Kursiv-Unterstrichen)), wie das Markdown benutzt werden kann. Dabei werden auch die nützlichsten Auszeichnungen aufgezählt und vorgeführt.

### Learnings
- Markdown ist eine Auszeichnungssprache, wie HTML, jedoch nur für Text
- Soll das Verfassen und Formatieren vereinfachen
- Markdown kann HTML Tags einbinden

### Quellen
Markdown Guide: <https://www.markdownguide.org/basic-syntax/#html>


## UNIX Shell und Virtual Machines
Bereits im Kurs Architektur von Informationssystemen (ARIS) hatten wir das Vergnügen mit der UNIX Shell zu arbeiten. Leider lernten wir in diesem Modul nicht viel über die UNIX Shell ausser, welche Befehle wir eintippen müssen. Was die [Commands](https://librarycarpentry.org/lc-shell/reference.html) tun, wurde uns nicht oder nur schlecht erklärt, weshalb ich mich damals selbst mit dem Thema auseinandersetzten musste. Wie auch in ARIS arbeiten wir in diesem Kurs wieder auf einer Virtual Machine (VM). Dieses Mal wird jedoch die VM nicht von uns gehostet, sondern von der Fachhochschule selbst (Danke an FH Graubünden). Dies hat einige simple Vorteile:
- bei Problemen mit der VM ist die Hochschule verantwortlich, um diese zu lösen.
- spart Speicherplatz auf der eigenen Festplatte
- VM könnten einfach übertragen und synchronisiert werden

Gleich vom ersten Punkt der Liste durfte ich in dieser Vorlesung profitieren. Meine VM konnte keine Verbindung zum Internet herstellen, obwohl ich an meinem Laptop keine Probleme mit der Internetverbindung feststellen konnte. Herr Lohmeier konnte dies der IT weitergeben und die behoben das Problem. Aufgrund dessen konnte ich jedoch die Carpentry Lessons nicht durchführen. Da ich jedoch bereits mit der UNIX Shell vertraut bin, habe ich nicht viel verpasst.

### Learnings:
- Bei Problemen nicht verzagen, Felix Lohmeier fragen.

Zeichen: 4002
