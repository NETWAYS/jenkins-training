!SLIDE bullets
# Installation
* Aus Paketen ...
* ... Oder eigener Container + .war

!SLIDE bullets incremental
# Paketinstallation
* Java installieren (mind. Version 1.7)

    @@@ Shell
    $ sudo yum install java

* Jenkins Repository hinzufügen

    @@@ Shell
    $ sudo yum install jenkins

~~~SECTION:notes~~~

Repository ist schon hinzugefügt.

~~~ENDSECTION~~~

!SLIDE center code
# Jenkins starten

    @@@ shell
    systemctl start jenkins

~~~SECTION:notes~~~

`systemctl status jenkins` für status

~~~ENDSECTION~~~

!SLIDE
# Jenkins läuft

Jenkins läuft nun local auf Port 8080

    `http://localhost:8080`
