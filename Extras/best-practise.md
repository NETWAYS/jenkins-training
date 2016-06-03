!SLIDE subsection
#~~~SECTION:MAJOR~~~ Best Practise

!SLIDE bullets 
#Backups, Backups, Backups
* Jenkins Konfiguration mit Hilfe von SCM sichern
* Tags für funktionierende Zustände
* Testen in Branches

!SLIDE smbullets
#Was soll man sichern?

* `$JENKINS_HOME/*.xml`
* `$JENKINS_HOME/jobs/*/*.xml`
* `$JENKINS_HOME/nodes/*`
* `$JENKINS_HOME/plugins/*.jpi`
* `$JENKINS_HOME/users/*`

* .gitignore hilft

!SLIDE smbullets 
#Die Testinstanz
* Ein sperater Jenkins-Test-Master erspaart viel kummer
  - Hardware muss nicht equivalent sein
* $JENKINS\_HOME in git einpflegen
  - Nur relevante Konfigurationsdateien in die Versionskontrolle
  - Artefakte, Logs etc. nicht
* Test-Agenten mit Docker o.ä. realisieren
* Kann per Merge einfach in Produktion genommen werden

!SLIDE bullets 
#Agilität durch Granularität
* Jobs in Teilschritte aufteilen:
  - Erlaubt Wiederverwendung von Modulen
  - Fehlerfindung/-behebung wird leichter
  - Schnellere Wiederaufnahme von fehlgeschlagenen Jobs
* Workflow/Pipeline Plugin

!SLIDE bullets 
#Agilität durch Granularität
* Mehrere Teams - Mehrere Master
  - Lastverteilung
  - Vermindert Plugin Bloat
* Unabhängige Projekte wenn möglich physisch trennen

!SLIDE bullets 
#Agilität durch Uniformität
* Uniforme Agenten sind leicht zu ersetzen
* Gleiche tools, gleiche Hardware
  - Gleiches Dockerfile
* Best Case: Agenten aus Foreman/Ansible etc.

~~~SECTION:notes~~~
Auf diese Art können unter Last oder bei Ausfall einfach neu Agenten
hinzugefügt werden. Auch skalierbar
Auf Foreman, Ansible Schulung hinweisen.
~~~ENDSECTION~~~
