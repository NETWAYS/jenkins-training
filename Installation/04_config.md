!SLIDE bullets
# Konfiguration
* Entweder im webinterface ...
* ... oder in Konfigdateien (XML-Format)

> Notiz:  
> Konfigdateien liegen im home Verzeichnis des jenkins-Benutzers.

!SLIDE smbullets
#Anzahl Executors ändern

> Notiz:  
> Executoren sind die "Arbeiter" einer Jenkins Instanz/Slaves.

!SLIDE bullets incremental
#Weboberfläche
* "Manage Jenkins"
* "Configure System"
* "# of executors" : 5
* Save

!SLIDE center noprint
#Konfigdateien
Per SSH auf den jenkins-master verbinden

    @@@ Shell
    ssh netways@192.168.52.50
    Password: netways

!SLIDE bullets incremental
#Konfigdateien
* `cd /var/lib/jenkins`
* `vim/emacs/ed config.xml`
* `<numExecutors>3<numExecutors>`

!SLIDE
#Konfigänderungen sichtbar machen
Nach solchen Änderungen muss Jenkins neu geladen oder neu gestartet werden.

Per Konsole:

    @@@ Shell
    systemctl restart jenkins

Per Webinterface:

    http://192.168.56.102:8080/reload  

> Notiz:  
> Auch Befehle wie 'restart' oder 'exit' können per url ausgeführt werden.

!SLIDE
#Backups von Jenkins
Änderungen im Webfrontend werden gleich in Konfigdateien geschreiben.
Auch jobs haben jeweils ihre eigenen config.xml Dateien.

Das komplette $JENKINS\_HOME Verzeichniss zu sichern kann aber zu sehr großen 
Backupdateien führen da sich dort auch Workspaces und build-Artefakte befinden.

https://gist.github.com/abayer/527063a4519f205efc74
