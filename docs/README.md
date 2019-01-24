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
In diesem Klassendiagramm sieht man die Datenkapselung der Daten vom Benutzer,Fake-Benutzer und Admin. 
![Klassendiagramm](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/KlassenDiagrammFindMe.svg)
Wie im Diagramm zu sehen erben Admin und Fake-Benutzer vom Benutzer da beide nur mehr Funktionen haben als ein Benutzer aber ansonsten gleich aufgebaut sind. und jede Nachricht beihaltet eine Nachricht, einen Sender und einen Empfänger. Diese Nachrichten landen in der Benutzer-Mailbox von jedem Benutzer

### SequenzDiagramm
Im folgenden sind zwei Sequenzdiagramme die den Ablauf einer Freundschaftanfrage zeigt und den Austausch von Nachrichten zwischen zwei Benutzern. Beide Funktionen sind in dem [UseCase-Diagramme](#UseCase-Diagramme) bereits gezeigt worden. 
![SeqAnfrage](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/SequenzDiagrammFindMeAnfrage.svg)
Dieses Diagramm zeigt den Vorgang einer Freundschaftanfrage. Dazu werden die Präferenzen von zwei Benutzern genutzt damit ein Benutzer den anderen in einer Suche finden kann. Benutzer A kann eine Freundschaftanfrage schicken und auf eine Antwort warten.
![SeqMail](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/SequenzDiagrammFindMeMails.svg)
Nachdem der Nutzer jemanden in seine Freundesliste hinzugefügt hat kann dieser z.B. mit der Person eine Unterhaltung führen.
Diesen Vorgang sind man in diesem Diagramm Benutzer A schreibt eine Nachricht die von seiner Mailbox in die Mailbox von Person B gesendet wird. Benutzer B kann nun die Nachricht lesen und antworten.

### Kommunikationsdiagramm
Im folgenden ist ein Diagramm das einmal den Kommunikationsvorgang zeigt der abläuft wenn ein Benutzer gemeldet wird.
![Kommunikationsdiagramm](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/KommunikationsDiagrammFindMe.svg)
Der Benutzer A meldet einen Benutzer nachdem dieser sich unangebracht geäußert hat. Ein Admin löscht daraufhin Benutzer B.

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

## Implementierungssicht

### Komponentendiagramm
![Komponentendiagramm](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/KomponentenDiagrammFindMe.svg)
Das Komponentendiagramm zeigt welche Komponente von welcher Komponenten ein Interface benötigt und kriegt.

## Paketdiagramm
![Paketdiagramm](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/PaketDiagrammFindMe.svg)
Das Diagramm zeigt in Paketen auf wo was von den [UseCase-Diagramme](#UseCase-Diagramme) sich befindet.

## Physikalische Sicht

### Verteilungsdiagramm
![Verteilungsdiagramm](https://agrellmann.github.io/SE-Softwarespezifikation/Diagramme/VerteilungFindMe.svg)  
Das Verteilungsdiagramm zeiht die Verteilung der Systemkomponenten auf die verschiedenen Systeme. Da das System von mobilen Endgeräten und Webbrowsern zugänglich sein soll, gibt es zwei Versionen. Die eine ist die Webseite, die als HTML-Dokument über den 
Webserver für die Webbrowser bereit gestellt wird. Dieser kommuniziert mit dem Applikationsserver, mit dem auch die mobilen Endgeräte kommunizieren. Die Applikation für diese beinhaltet die HTML-Datei in einer für die Geräte optimisierten Form und bietet 
darüber den Zugang zu jeglichen Funktionen. Auf dem Applikationsserver läuft das Backend wie z.B. der Suchalgorithmus zum Matchen der Usern. Die Daten sind auf einem Datenbankserver gelagert, auf den der Webserver und der Applikationsserver Zugriff hat.

## GUI-Mockup

In diesem Abschnitt ist das GUI-Mockup zu dem Programm bzw. der Webseite find.me zu finden. Es ist für die Webseite konzipiert worden, kann aber auch mit kleinen Veränderungen so für Mobilgeräte übernommen werden.
Diese Veränderungen sind z.B. das Anpassen der Breite des "Inhaltsstreifens" und das Ändern der Indexseite der Webseite, sodass diese an das Konzept von Mobilgeräten angepasst wird.

[GUI-Mockup-PDF](https://agrellmann.github.io/SE-Softwarespezifikation/FindMeGui/FindMeGui.pdf)
