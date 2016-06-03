!SLIDE subsection
# ~~~SECTION:MAJOR~~~ Security

!SLIDE bullets noprint
#Userauth
* Jenkins eigene Datenbank (Mit signup)
* LDAP
* Unix bassiert
* AD (Windows)
* Per Webserver

!SLIDE bullets noprint
#Rechte Management
* Nur Read/Write
* Per matrix

~~~SECTION:notes~~~

Viele der Security features sind addons die standard dabei sind
Für Unix auth brauch der user unter dem jenkins läuft rechte auf /etc/shadow

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Zusätzliche Tipps
* Jenkins hat im Zweifel totale Kontrolle über alle Slaves
 - Auf Slaves extra Jenkins User verwenden (mit eigenem ssh key)
* Offene Jenkins Installationen sind nicht unüblich
 - Keine Passwörter o.Ä. in Job-Skripten verwenden

!SLIDE smbullets printonly
#Userauth
* Jenkins eigene Datenbank (Mit signup)
* LDAP
* Unix bassiert
* AD (Windows)
* Per Webserver

!SLIDE smbullets printonly
#Rechte Management
* Nur Read/Write
* Per matrix

~~~SECTION:notes~~~

Viele der Security features sind addons die standard dabei sind
Für Unix auth brauch der user unter dem jenkins läuft rechte auf /etc/shadow

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Zusätzliche Tipps
* Jenkins hat im Zweifel totale Kontrolle über alle Slaves
 - Auf Slaves extra Jenkins User verwenden (mit eigenem ssh key)
* Offene Jenkins Installationen sind nicht unüblich
 - Keine Passwörter o.Ä. in Job-Skripten verwenden

