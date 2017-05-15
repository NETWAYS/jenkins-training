!SLIDE bullets noprint
#Userauth
* Own Jenkins database (does signup)
* LDAP
* Unix
* AD (Windows)
* HTTP AUTH (Webserver)

!SLIDE bullets noprint
#Permission Management
* Read/write only
* Matrix

~~~SECTION:notes~~~

Viele der Security features sind addons die standard dabei sind
Für Unix auth brauch der user unter dem jenkins läuft rechte auf /etc/shadow

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Pro-tips
* Use a dedicated user with SSH key on every slave
 - Reduce security issues that somebody gains control on every slave
* No passwords in job scripts
  - Even less when Jenkins is public

!SLIDE smbullets printonly
# Userauth
* Own Jenkins database (also Signup)
* LDAP
* Unix
* AD (Windows)
* HTTP AUTH (Webserver)

!SLIDE smbullets printonly
# Permission Management
* Read/Write only
* Matrix

~~~SECTION:notes~~~

Viele der Security features sind addons die standard dabei sind
Für Unix auth brauch der user unter dem jenkins läuft rechte auf /etc/shadow

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Pro-tips
* Use a dedicated user with SSH key on every slave
 - Reduce security issues that somebody gains control on every slave
* No passwords in job scripts
  - Even less when Jenkins is public
