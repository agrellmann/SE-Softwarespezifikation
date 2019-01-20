# Software Engineering Softwarespezifikation

[User Stories](UserStories.md ':include')

## Szenarien

### UseCase-Diagramme
![UseCase Gesamt](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseGesamt.svg)
![UseCase Kommunikation](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseKommunikation.svg)
![UseCase Admin](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseAdmin.svg)
![UseCase Fake-User](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseFake-User.svg)
![UseCase Suchen](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/UseCaseFindMe/UseCaseSuchen.svg)

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
