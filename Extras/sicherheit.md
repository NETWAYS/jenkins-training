!SLIDE bullets noprint
#Userauth
* Jenkins own database (does signup)
* LDAP
* Unix
* AD (Windows)
* HTTP AUTH (Webserver)
  - No public Jenkins possible

!SLIDE bullets noprint
#Permission Management
* Applies to users within Jenkins
* Simple
 - Anybody/Loggied in can do everything
* Matrix
 - Project or User/Group base
 - Can't inherit from userauth

~~~SECTION:notes~~~

Viele der Security features sind addons die standard dabei sind
Für Unix auth brauch der user unter dem jenkins läuft rechte auf /etc/shadow

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Pro-tips
* Use a dedicated user with their own SSH key on every slave
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
  - No public Jenkins possible

!SLIDE smbullets printonly
# Permission Management
* Applies to users within Jenkins
* Simple
 - Anybody/Loggied in can do everything
* Matrix
 - Project or User/Group base
 - Can't inherit from userauth


~~~SECTION:notes~~~

Viele der Security features sind addons die standard dabei sind
Für Unix auth brauch der user unter dem jenkins läuft rechte auf /etc/shadow

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Pro-tips
* Use a dedicated user with their own SSH key on every slave
 - Reduce security issues that somebody gains control on every slave
* No passwords in job scripts
  - Even less when Jenkins is public
