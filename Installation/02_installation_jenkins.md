!SLIDE bullets
# Installation
* Java  (jdk > 1.7)
* Optional: Tomcat, Glassfish, ...
* Entweder
 - Packet
 - jenkins.war

~~~SECTION:notes~~~
~~~ENDSECTION~~~

!SLIDE
#Installation
Im Home-Verzeichniss des Nutzers (/home/jenkins) liegt ein .deb file bereit.
Installation via:

    @@@ shell
    sudo dpkg -i jenkins_1.644_all.deb

!SLIDE
# Jenkins starten
Via systemd/init

    @@@ shell
    systemctl start jenkins

!SLIDE
# Jenkins läuft

Jenkins läuft auf Port 8080

    @@@ shell
    http://172.16.32.10:8080
