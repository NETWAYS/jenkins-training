!SLIDE bullets noprint
# Installation
* Java (JDK > 1.7)
* Optional: Tomcat, Glassfish, ...
* Entweder
 - Paket
 - jenkins.war

~~~SECTION:notes~~~
Tomcat wird nur gebruacht wenn man es manuel startet
~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Installation
* Java (JDK > 1.7)
* Optional: Tomcat, Glassfish, ...
* Entweder
 - Paket
 - jenkins.war

!SLIDE
# Installation
Im Home-Verzeichnis des Nutzers (/home/training) liegt ein .deb file bereit.
Installation via:

    @@@ shell
    $ sudo dpkg -i jenkins_1.644_all.deb

!SLIDE
# Jenkins starten
Via systemd/init

    @@@ shell
    $ sudo systemctl start jenkins

!SLIDE
# Jenkins läuft

Jenkins läuft auf Port 8080

    @@@ shell
    http://jenkins-master:8080
