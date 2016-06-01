!SLIDE subsection
#~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~ Jenkins Agent erstellen

!SLIDE bullets
#Einen Jenkins Agenten hinzufügen

* `Manage Jenkins` -> `Manage Nodes`
* `Node Name` + 'Dumb Slave'
* `Host` : 'jenkins-agent'
* `Credentials` auswählen

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

* Entweder Executoren des Masters auf 0 stellen
* Oder dem Agenten ein label geben und im Beispielprojekt eintragen

!SLIDE center  norpint 
#Fehlschlag
Was ging schief?

Das Paket python-virtualenv fehlt

~~~SECTION:notes~~~

Teilnehmer fragen

~~~ENDSECTION~~~

!SLIDE bullets
#Nodes provisionieren
`python-virtualenv` (oder andere tools) via jenkins installieren.

* Neues Freestyle Projekt
* 'This Build is parameterized'
 - Name wird als Umgebungsvariable exportiert

Build step:

    @@@ sh
    apt-get install $tool -y

~~~SECTION:notes~~~

-y Da Jenkins nicht interaktiv ist

~~~ENDSECTION~~~

