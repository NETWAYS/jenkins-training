!SLIDE subsection
#~~~SECTION:MAJOR~~~ Configuration

!SLIDE bullets noprint
# Configuration
Jenkins can be configured in two ways
* Through the web interface
* By editing it's config files (XML-formated)

~~~SECTION:notes~~~
Konfigdateien liegen im Homeverzeichnis des jenkins-Benutzers.
~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Configuration
Jenkins can be configured in two ways
* Through the web interface
* By editing it's config files (XML-formated)

# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: The Two Ways Of Configuration

* Objective:
 * Change the number of executors
* Steps:
 * Navigate to the `Manage Jenkins`-menu
 * `Configure System` to change the number of executors to 5
 * shh into the jenkins master (`ssh jenkins-master, passwd 'netways'`)
 * Find the 'Jenkins-Home' at `/var/lib/jenkins`
 * Edit the `config.xml` and set the executors back to 3
 * Reload Jenkins 

!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: The Two Ways Of Configuration

## Objective:

****

* Change the number of executors

## Steps:

****

* Navigate to the `Manage Jenkins`-menu
* `Configure System` to change the number of executors to 5
* shh into the jenkins master (`ssh jenkins-master, passwd 'netways'`)
* Find the 'Jenkins-Home' at `/var/lib/jenkins`
* Edit the `config.xml` and set the executors back to 3
* Reload Jenkins 

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## The Two ways of Configuration

****

## Webinterface:

 TODO: SCREENSHOTS

## Configuration Files:

  # cd /var/lib/jenkins
  # vim config.xml

    `<numExecutors>3</numExecutors>`

  # sudo systemctl restart jenkins


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
