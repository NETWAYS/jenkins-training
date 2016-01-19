!SLIDE center
#Architektur
<img src="./_img/Jenkins System.svg" alt="Jenkins System"/>

~~~SECTION:notes~~~

Container: Ein Java-Webserver (Alternativen: Glassfish, Geronimo)  
Jenkins: Jenkins Java application (.WAR)  
Rest: Andere Jenkins Applikationen, Executoren eigendlich teil von jenkins sind
aber optional.
Datenbank: Alle Config Datein in XML in Jenkins Home (defaut: /var/lib/jenkins)

~~~ENDSECTION~~~

!SLIDE bullets printonly
* Jenkins liegt in einem Container (Tomcat, Glasfish...)
* Alle Konfiguration wird als xml im Jenkins Home gespeichert
* Jenkins kann mit anderen Jenkins Instanzen kommunizieren


