!SLIDE subsection
#Best Practise

!SLIDE bullets incremental
#Backups, Backups, Backups
* Jenkins Konfiguration mit hilfe eines scm sichern
* Tags für funktionierende Zustände
* Testen in branches

!SLIDE smbullets incremental
#Die Testinstanz
* Ein sperater Jenkins-Test-Master erspaart viel kummer
  - Hardware muss nicht equivalent sein
* $JENKINS\_HOME in git einpflegen
  - Nur relevante Konfigurationsdateien in die Versionskontrolle
  - Artefakte, Logs etc. nicht
* Test-Agenten mit Docker o.Ä. realisieren
* Kann per merge einfach in Produktion genommen werden

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
  - Vermindert plugin bloat
* Unabhängige Projekte wenn möglich physisch trennen
