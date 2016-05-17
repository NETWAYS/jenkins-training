!SLIDE bullets
# Installation
* Java  (jdk > 1.7)
* Optional: Tomcat, Glassfish, ...
* Entweder
 - Packet
 - jenkins.war

~~~SECTION:notes~~~

Repository ist schon hinzugefügt.

~~~ENDSECTION~~~

!SLIDE bullets
# Jenkins starten

* Mit Container
* Via systemd/init

    @@@ shell
    systemctl start jenkins

!SLIDE
# Jenkins läuft

Jenkins läuft auf Port 8080

    @@@ shell
    http://192.168.56.50:8080
