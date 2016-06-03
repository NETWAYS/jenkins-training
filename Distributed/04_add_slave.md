!SLIDE subsection
#~~~SECTION:MAJOR~~~ Jenkins Agent erstellen

!SLIDE center
#Los gehts!
Starten sie den Jenkins Agenten

!SLIDE bullets
#Einen Jenkins Agenten hinzufügen

* `Manage Jenkins` -> `Manage Nodes`
* `Node Name` + 'Dumb Slave'
* `Host` : '192.168.56.102'
* `Credentials` auswählen
* `Remote root directory`: '/home/jenkins'

~~~SECTION:notes~~~

Slave/Agent erklären
Node: Master und Agenten sind Nodes
Es gibt keine noch keine 'smart' slaves
Label restrictions: bsp windows
Startet automatisch nach save

~~~ENDSECTION~~~

!SLIDE center noprint
#Arbeit verteilen
Das Beispielprojekt soll nur auf dem Agenten gebaut werden

~~~SECTION:notes~~~

Die Teilnehmer können das selbst versuchen.
Lösungen:
Master executoren wegnehmen
Agenten label hinzufügen und bei Projekt eintragen

~~~ENDSECTION~~~

!SLIDE bullets printonly
#Arbeit verteilen
Das Beispielprojekt soll nur auf dem Agenten gebaut werden

Dazu sollten labels verwendet werden.

!SLIDE center norpint
#Fehlschlag
Was ging schief?

~~~SECTION:notes~~~

Teilnehmer fragen

~~~ENDSECTION~~~

!SLIDE bullets
#Fehlschlag
* Der Agent hat keinen Zugriff auf das Repository am Master
* `localhost` auf `192.168.56.101` ändern
* Credentials eintragen

~~~SECTION:notes~~~

Credentials werden vom master and Agenten weitergereicht

~~~ENDSECTION~~~
