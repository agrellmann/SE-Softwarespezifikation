# Software Engineering Softwarespezifikation

Dies ist die Ausarbeitung zu der zweiten Software Engineering Aufgabe, in der wir die Softwarespezifikation erstellen mussten. Dabei haben wir uns an dem 4+1-Sichten Modell orientiert.
Das [GUI-Mockup](#GUI-Mockup) ist am Ende als PDF zu finden.

## User-Stories

In diesem Abschnitt stehen die, aus dem Vorgabedokument extrahierten, User Stories und evtl. Akzeptanzkriterien.
Die [Aktivitäts](#Aktivitätsdiagramme) und [UseCase](#UseCase-Diagramme)-Diagramme dazu sind im laufenden Dokument zu sehen.

[User Stories](UserStories.md ':include')

## Szenarien

### UseCase-Diagramme
In diesem Abschnitt sind die UseCase-Diagramme zu den [User-Stories](#User-Stories). Aufgeteilt sind diese in einer Gesamtübersicht und den einzelen UseCases zur Kommunikation, dem Suchen, den Adminvorgängen und den Fake-User-Vorgängen.  
![UseCase Gesamt](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseGesamt.svg)  
Das Diagramm _Gesamt_ ist die Übersicht über die Vererbungen der Akteure (Admin und Fake-User erben von dem normalen User) und die UseCase-Gruppen die dazu gehören. Diese sind im Folgenden weiter aufgeführt.  
![UseCase Kommunikation](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseKommunikation.svg)  
Das Diagramm _Kommunikationsvorgänge_ zeigt die UseCases, die zur Kommunikation der User gehört. Dazu zählen z.B. Schreiben und Lesen von Nachrichten oder auch Freundschftsanfragen.  
![UseCase Suchen](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseSuchen.svg)  
Das Diagramm _Suchvorgänge_ zeigt die UseCases, die zum Suchen von passenden Benutzern gehören. Dafür müssen die eigenen Präferenzen angegeben werden und können danach im gesamten oder nur teilweise gesucht und die gefundenen Benutzer angesehen werden.  
![UseCase Admin](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseAdmin.svg)  
Das Diagramm _Adminvorgänge_ zeigt die Zusatzfunktionen, die Admins über normale User haben. Diese beschränken sich bisher auf das Auflisten gemeldeter Nutzer und das löschen dieser.  
![UseCase Fake-User](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseFake-User.svg)  
Das Diagramm _Fake-User-Vorgänge_ zeigt die Zusatzfunktionen, die ein Fake-User über einen normalen Benutzer besitzt. Dieser kann mehrere Profile mit einem Benutzer haben und verwalten und damit wie mit normalen Profilen umgehen.

## Logische Sicht

### Klassendiagramm
![Klassendiagramm](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/KlassenFindMe.svg)

## Prozesssicht

### Aktivitätsdiagramme
In diesem Abschnitt sind die Aktivitätsdiagramme zu den komplexeren UseCases der [UseCase-Diagramme](#UseCase-Diagramme).  
![MainClient](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/AktivitaetFindMe/MainClientKommunikation.svg)
Das Diagramm _Main Client Kommunikation_ zeigt eine normale Benutzung des Programmes bzw. der Webseite. Dabei wird von dem Start des Programmes bzw. dem Aufrufen der Webseite als Startpunkt ausgegangen.
Daher fängt das Diagramm mit dem Anmelden bzw. der Profilerstellung an. Die Vorgänge dazu sind im folgenden weiter ausgeführt.
![Anmelden](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/AktivitaetFindMe/Anmelden.svg)
Das Diagramm _Anmelden_ zeigt den Anmeldevorgang, der bei dem Benutzer anfängt, der zuerst seinen Benutzername und sein Password eingeben muss und diese dann abschickt. Das System prüft diese dann und lässt den 
User sich entweder einloggen oder gibt ihm einen neuen Versuch.
![Profil Erstellen](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/AktivitaetFindMe/ProfilErstellen.svg)
Das Diagramm _Profil Erstellen_ zeigt den Vorgang der Erstanmeldung, bei dem mit dem Prüfen nach einem vorhandenen Account begonnen und falls keiner vorhanden ist die Profilerstellung eingeleitet wird.
Danach müssen die Profilinfos angegeben und verifiziert werden. Wenn diese verifiziert werden konnten, kommt man zu weiteren Profileinstellungen und kann danach weiter auf der Plattform agieren (s. _Main Client Kommunikation_).
![Vorgeschlagende Benutzerliste ansehen](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/AktivitaetFindMe/vorgeschlagendeBenutzerlisteAnsehen.svg)
Das Diagramm _Vorgeschlagende Benutzerliste ansehen_ zeigt die Vorgänge, die zum Ansehen der Liste mit den vorgechlagenden Benutzern, nötig sind. Dabei kann man entweder nach einzelnen Präferenzen suchen (Präferenzen auswählen) 
oder direkt nach passenden Benutzern suchen. Danach erstellt das System die passende Benutzerliste und sendet diese zurück zum User, der sich diese ansehen kann und weitere Aktionen, wie Löschen oder Freundesanfrage, einleitet.

## Physikalische Sicht

### Verteilungsdiagramm
![Verteilungsdiagramm](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/VerteilungFindMe.svg)

## GUI-Mockup

In diesem Abschnitt ist das GUI-Mockup zu dem Programm bzw. der Webseite find.me zu sehen. Es ist für die Webseite konzipiert worden, kann aber auch mit kleinen Veränderungen so für Mobilgeräte übernommen werden.
Diese Veränderungen sind z.B. das Anpassen der Breite des "Inhaltsstreifens" und das Ändern der Indexseite der Webseite, sodass diese an das Konzept von Mobilgeräten angepasst wird.

[GUI-Mockup-PDF](https://agrellmann.github.io/SE-Softwarespezifikation/FindMeGui/FindMeGui.pdf)
