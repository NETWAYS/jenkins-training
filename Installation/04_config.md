!SLIDE subsection
#~~~SECTION:MAJOR~~~ Konfiguration

!SLIDE bullets noprint
# Konfiguration
* Entweder im Webinterface ...
* ... oder in Konfigdateien (XML-Format)

~~~SECTION:notes~~~
Konfigdateien liegen im Homeverzeichnis des jenkins-Benutzers.
~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Konfiguration
* Entweder im Webinterface ...
* ... oder in Konfigdateien (XML-Format)

!SLIDE noprint
#Anzahl Executors ändern
Einfache Übungsaufgabe:  
  Ändern der Executoren über beide Wege

~~~SECTION:notes~~~
Executoren sind die "Arbeiter" einer Jenkins Instanz/Agents.
~~~ENDSECTION~~~

!SLIDE bullets noprint
#Weboberfläche
* "Manage Jenkins"
* "Configure System"
* "# of executors" : 5
* Save

!SLIDE smbullets printonly
#Weboberfläche
* "Manage Jenkins"
* "Configure System"
* "# of executors" : 5
* Save

!SLIDE center noprint
#Konfigdateien
Per SSH auf den jenkins-master verbinden

    @@@ Shell
    ssh jenkins-master
    Password: netways

!SLIDE bullets noprint
#Konfigdateien
* `cd /var/lib/jenkins`
* `vim/emacs/ed config.xml`
* `<numExecutors>3</numExecutors>`

!SLIDE smbullets printonly
#Konfigdateien
* `cd /var/lib/jenkins`
* `vim/emacs/ed config.xml`
* `<numExecutors>3</numExecutors>`

!SLIDE
#Konfigänderungen sichtbar machen
Nach solchen Änderungen muss Jenkins neu geladen oder neu gestartet werden.

Per Konsole:

    @@@ Shell
    sudo systemctl restart jenkins

Per Webinterface:

	`Manage Jenkins` -> `Reload Configuration from Disk`

Per API:

    http://jenkins-master:8080/reload  



~~~SECTION:notes~~~
Auch Befehle wie 'restart' oder 'exit' können per url ausgeführt werden.
TODO: Add to cheatsheet
~~~ENDSECTION~~~

!SLIDE
#Backups von Jenkins
Änderungen im Webfrontend werden gleich in Konfigdateien geschreiben.
Auch Jobs haben jeweils ihre eigenen config.xml Dateien.

Das komplette $JENKINS\_HOME Verzeichnis zu sichern kann aber zu sehr großen 
Backupdateien führen, da sich dort auch Workspaces und build-Artefakte befinden.

~~~SECTION:notes~~~
https://gist.github.com/abayer/527063a4519f205efc74
~~~ENDSECTION~~~
