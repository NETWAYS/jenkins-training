!SLIDE subsection
#~~~SECTION:MAJOR~~~ Credentials

!SLIDE bullets noprint
#Crendentials
* ... Haben eine Domain (Gruppe)
* ... Ein Scope (Sichtbarkeit)
* ... Einen Typ  
	(Name+Passwort, Zertifikat..)

~~~SECTION:notes~~~

Domains zur Übersicht, keine neue Erstellen
Scope: System?
Gleich die Credentials eintragen lassen

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Credentials eintragen
* Domain 'Global credentials' wählen
 - Kind: 'SSH Usermane with private key'
 - Username: `jenkins`
 - `Private Key`: `From the Jenkins master ~/.ssh`
 - ID und Description können frei gelassen werden

~~~SECTION:notes~~~
~~~ENDSECTION~~~

!SLIDE bullets noprint
#Credentials eintragen
* Auf den Agent (192.168.56.102) als `training` verbinden
* id\_rsa.pub (vom master) in authorized\_keys eintragen





!SLIDE smbullets printonly
#Crendentials
* ... Haben eine Domain (Gruppe)
* ... Ein Scope (Sichtbarkeit)
* ... Einen Typ  
	(Name+Passwort, Zertifikat..)

!SLIDE smbullets printonly
#Credentials eintragen
* Domain 'Global credentials' wählen
 - Kind: 'SSH Usermane with private key'
 - Username: `jenkins`
 - `Private Key`: `From the Jenkins master ~/.ssh`
 - ID und Description können frei gelassen werden

!SLIDE smbullets printonly
#Credentials eintragen
* Auf den Agent (192.168.56.102) als `training` verbinden
* id\_rsa.pub (vom master) in authorized\_keys eintragen
