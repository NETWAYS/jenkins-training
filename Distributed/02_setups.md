!SLIDE subsection
#~~~SECTION:MAJOR~~~ Architektur und Startup

!SLIDE center noprint
#Was wir schon haben
<img src="./_img/Jenkins_Server_Single.svg" alt="Single Server"/>

~~~SECTION:notes~~~

Eine Installation mit beliebig vielen Executoren

~~~ENDSECTION~~~

!SLIDE printonly
#Was wir schon haben
<center><img src="./_img/Jenkins_Server_Single.svg" style="width:600" alt="Single Server"/><center>

!SLIDE center noprint
#Was wir wollen
<img src="./_img/Jenkins_Server_Multi.svg" alt="Multi Server"/>

~~~SECTION:notes~~~

Volles Jenkins nur auf Master.
Webserver nur auf Master.
Agents werden vom master via ssh autmatisch installiert und gestartet.
Kommunikation via tcp/ip.

~~~ENDSECTION~~~

!SLIDE printonly
#Was wir wollen
<center><img src="./_img/Jenkins_Server_Multi.svg" style="width:480;height:267px" alt="Multi Server"/></center>

!SLIDE
#Agent via SSH
Master benötigt nur SSH-Zugangsdaten zum Server des Agenten, der Rest
geschieht automatisch.

Eventuelle Tools (python, virtualenv...) die zum ausführen von Jobs gebraucht
werden, müssen selbst installiert werden.

~~~SECTION:notes~~~

Tools sind schon vorinstalliert (ausser virtualenv, geplanter fehlschlag)

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Alternative Startmöglichkeiten
* WMI und DOM auf Windows
* JNLP (Grafisch)
* Eigenes Script
 - Jenkins verwendet stdin/out zur Kommunikation.

~~~SECTION:notes~~~

JNLP: Java Network Launch Protocol
Eigenes Script: slave.jar kommuniziert nicht von selbst mit jenkins

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Alternative Startmöglichkeiten
* WMI und DOM auf Windows
* JNLP (Grafisch)
* Eigenes Script
 - Jenkins verwendet stdin/out zur Kommunikation.

