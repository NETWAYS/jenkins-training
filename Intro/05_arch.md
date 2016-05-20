!SLIDE center
#Architektur
<img src="./_img/Jenkins System.svg" alt="Jenkins System"/>

~~~SECTION:notes~~~

Container: Ein Java-Webserver (Alternativen: Glassfish, Geronimo)  
Jenkins: Jenkins Java application (.WAR)  
Config: Als XML in $JENKINS\_HOME, z.B /var/lib/jenkins
Executoren: Plätze auf denen Jobs laufen können.
Es laufen maximal so viele Jobs parallel wie Executoren frei sind


~~~ENDSECTION~~~

!SLIDE bullets printonly
* Jenkins liegt in einem Container (Tomcat, Glasfish...)
* Alle Konfiguration wird als XML im Jenkins Home gespeichert
* Jenkins kann mit anderen Jenkins-Instanzen kommunizieren

