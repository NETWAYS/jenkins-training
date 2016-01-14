!SLIDE smbullets
# Installation
* Aus Paketen ...
* ... Oder eigener Container + .war

!SLIDE smbullets
#Paketinstallation
* Jenkins Repository hinzufügen

    apt install jenkins

~~~SECTION:notes~~~

Repository ist schon hinzugefügt.

~~~ENDSECTION~~~

!SLIDE smbullets
#Jenkins starten

    @@@ shell
    systemctl start jenkins

> Notiz:
> Mit tomcat schlägt der Jenkins-Start meist fehl
> Port muss geändert werden in `/etc/default/jenkins`

> Notiz:
> Port 80 kann per iptables umgeleitet werden
