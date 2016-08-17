!SLIDE subsection
#~~~SECTION:MAJOR~~~ Creating A Jenkins Agent

!SLIDE bullets noprint
# Adding The Jenkins Agent
* `Manage Jenkins` -> `Manage Nodes`
* `Node Name` + 'Dumb Slave'
* `Host` : '192.168.56.102'
* Choose Credentials `Credentials`
* `Remote root directory`: '/home/training'

~~~SECTION:notes~~~

Vielleicht /home/jenkins statt training, TODO herausfinden
Slave/Agent erklären
Node: Master und Agenten sind Nodes
Es gibt keine noch keine 'smart' slaves
Label restrictions: bsp windows
Startet automatisch nach save

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Adding The Jenkins Agent
* `Manage Jenkins` -> `Manage Nodes`
* `Node Name` + 'Dumb Slave'
* `Host` : '192.168.56.102'
* Choose Credentials `Credentials`
* `Remote root directory`: '/home/training'

!SLIDE center noprint
# Reassigning The Work
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

!SLIDE center noprint
#Fehlschlag
Was ging schief?

~~~SECTION:notes~~~

Teilnehmer fragen

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Fehlschlag
* Der Agent hat keinen Zugriff auf das Repository am Master
* `localhost` auf `192.168.56.101` ändern
* Credentials eintragen

~~~SECTION:notes~~~

Credentials werden vom master and Agenten weitergereicht

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Fehlschlag
* Der Agent hat keinen Zugriff auf das Repository am Master
* `localhost` auf `192.168.56.101` ändern
* Credentials eintragen

