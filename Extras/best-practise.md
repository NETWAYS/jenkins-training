!SLIDE subsection
#Best Practise

!SLIDE bullets incremental
#Backups, Backups, Backups
* Jenkins Konfiguration mit Hilfe von SCM sichern
* Tags für funktionierende Zustände
* Testen in Branches

!SLIDE smbullets incremental
#Die Testinstanz
* Ein sperater Jenkins-Test-Master erspaart viel kummer
  - Hardware muss nicht equivalent sein
* $JENKINS\_HOME in git einpflegen
  - Nur relevante Konfigurationsdateien in die Versionskontrolle
  - Artefakte, Logs etc. nicht
* Test-Agenten mit Docker o.ä. realisieren
* Kann per Merge einfach in Produktion genommen werden

!SLIDE bullets incremental
#Agilität durch Granularität
* Jobs in Teilschritte aufteilen:
  - Erlaubt Wiederverwendung von Modulen
  - Fehlerfindung/-behebung wird leichter
  - Schnellere Wiederaufnahme von fehlgeschlagenen Jobs
* Workflow/Pipeline Plugin

!SLIDE bullets incremental
#Agilität durch Granularität
* Mehrere Teams - Mehrere Master
  - Lastverteilung
  - Vermindert Plugin Bloat
* Unabhängige Projekte wenn möglich physisch trennen

!SLIDE bullets incremental
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
