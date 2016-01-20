!SLIDE subsection
# ~~~SECTION:MAJOR~~~ Security

!SLIDE bullets
#Userauth
* Jenkins eigene Datenbank (Mit signup)
* LDAP
* Unix bassiert
* AD (Windows)
* Per Webserver

!SLIDE bullets
#Rechte Management
* Nur Read/Write
* Per matrix

~~~SECTION:notes~~~

Viele der Security features sind addons die standard dabei sind
Für Unix auth brauch der user unter dem jenkins läuft rechte auf /etc/shadow

~~~ENDSECTION~~~

!SLIDE bullets
#Zusätzliche Sicherheit
* CSRF Schutz mit Crumbs
 Jenkins ist mä
