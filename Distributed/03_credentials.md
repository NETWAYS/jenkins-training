!SLIDE subsection
#~~~SECTION:MAJOR~~~ Credentials

!SLIDE bullets
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

!SLIDE bullets
#Credentials eintragen
* Domain 'Global credentials' wählen
 - Kind: 'SSH Usermane with private key'
 - Username: `jenkins`
 - `Private Key`: `From the Jenkins master ~/.ssh`
 - ID und Description können frei gelassen werden

~~~SECTION:notes~~~
~~~ENDSECTION~~~

!SLIDE bullets
#Credentials eintragen
* Auf den Agent (192.168.56.102) als `training` verbinden
* id\_rsa.pub (vom master) in authorized\_keys eintragen
