!SLIDE subsection
#~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~ Jenkins Agent erstellen

!SLIDE bullets
#Einen Jenkins Agenten hinzufügen

* `Manage Jenkins` -> `Manage Nodes`
* `Node Name` + 'Dumb Slave'
* `Host` : '172.16.32.20'
* `Credentials` auswählen

~~~SECTION:notes~~~

Schlechte idee jenkins als root laufen zu lassen
Node: Master und Agenten sind Nodes
TODO: Beispiel 'smart Slaves' 
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

!SLIDE center incremental norpint 
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

