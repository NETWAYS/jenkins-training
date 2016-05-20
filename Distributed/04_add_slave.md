!SLIDE bullets
#Einen Jenkins Agenten hinzufügen

* `Manage Jenkins` -> `Manage Nodes`
* `Node Name` + 'Dumb Slave'
* `Host` : "192.168.56.200"
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

    @@@ Bash
    apt-get install $tool -y

~~~SECTION:notes~~~

-y Da Jenkins nicht interaktiv ist

~~~ENDSECTION~~~

!SLIDE center noprint
#Jobs verketten
`Post-Build Action` -> `Build Other Projects`
So das Beispielprojekt gleich danach bauen

~~~SECTION:notes~~~

Erklärung nächste Folie

~~~ENDSECTION~~~

!SLIDE smbullets
#Jobs verketten
Verkettete Jobs erlauben es komplexe oder langsame Jobs in kurze Abschnitte
auszuteilen.

* Schnelleres Wiederaufnehmen von gescheiterten Jobs
* Wiederverwendung von generischen Jobs
* Workflow/Pipleine plugin hilft
