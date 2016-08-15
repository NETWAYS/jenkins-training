!SLIDE bullets noprint
# Installation
* Java (JDK > 1.7)
* Optional: Tomcat, Glassfish, ...
* Two common ways
 - Paket
 - jenkins.war

~~~SECTION:notes~~~
Tomcat wird nur gebaucht wenn man es manuel startet
~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Installation
* Java (JDK > 1.7)
* Optional: Tomcat, Glassfish, ...
* Two common ways
 - Paket
 - jenkins.war

!SLIDE
# Installation
Jenkins is already 'installed'
* Jenkins version 2.7.2 in `/home/jenkins`
* Unit file in `/etc/systemd/system`

!SLIDE
# Starting Jenkins
Start via systemctl

    @@@ shell
    $ sudo systemctl start jenkins

!SLIDE
# Jenkins is now running

By default Jenkins runs on port 8080

    @@@ shell
    http://jenkins-master:8080
