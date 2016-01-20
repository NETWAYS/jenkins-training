!SLIDE bullets
#Einen Jenkins Slave hinzufügen

* Credentials eintragen:  
  root:netways@192.156.24.1 TODO: richtige daten eintragen
* `Manage Jenkins` -> `Manage Nodes`
* `Node Name` + 'Dumb Slave'
* `Host` eintragen und `Credentials` wählen

~~~SECTION:notes~~~

Schlechte idee jenkins als root laufen zu lassen
Node: Master und Slaves sind Nodes
TODO: Beispiel 'smart' Slave
Label restrictions: bsp windows
Startet automatisch nach save

~~~ENDSECTION~~~

!SLIDE center noprint
#Arbeit verteilen
Das Beispielprojekt soll nur auf dem Slave gebaut werden

~~~SECTION:notes~~~

Die Teilnehmer können das selbst versuchen.
Lösungen:
Master executoren wegnehmen
Slave label hinzufügen und bei Projekt eintragen

~~~ENDSECTION~~~

!SLIDE bullets printonly
#Arbeit verteilen
Das Beispielprojekt soll nur auf dem Slave gebaut werden

* Entweder Executoren des Masters auf 0 stellen
* Oder dem Slave ein label geben und im Beispielprojekt eintragen

!SLIDE center incremental norpint 
#Fehlschlag
Was ging schief?

Das Paket python-virtualenv fehlt

~~~SECTION:notes~~~

Teilnehmer fragen

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Der Fix
`python-virtualenv` via jenkins installieren.

    @@@ Bash
    yum install python-virtualenv -y

~~~SECTION:notes~~~

-y Da Jenkins nicht interaktiv ist
Nochmal erwähnen das build jobs nicht als root laufen sollten

~~~ENDSECTION~~~
