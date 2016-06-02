!SLIDE subsection
#~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~ Architektur und Startup

!SLIDE center
#Was wir schon haben
<img src="./_img/Jenkins_Server_Single.svg" alt="Single Server"/>

~~~SECTION:notes~~~

Eine Installation mit beliebig vielen Executoren

~~~ENDSECTION~~~

!SLIDE center
#Was wir wollen
<img src="./_img/Jenkins_Server_Multi.svg" alt="Multi Server"/>

~~~SECTION:notes~~~

Volles Jenkins nur auf Master.
Webserver nur auf Master.
Agents werden vom master via ssh autmatisch installiert und gestartet.
Kommunikation via tcp/ip.

~~~ENDSECTION~~~

!SLIDE
#Agent via SSH
Master benötigt nur SSH-Zugangsdaten zum Server des Agenten, der Rest
geschieht automatisch.

Eventuelle Tools (python, virtualenv...) die zum ausführen von Jobs gebraucht
werden, müssen selbst installiert werden.

~~~SECTION:notes~~~

Tools sind schon vorinstalliert (ausser virtualenv, geplanter fehlschlag)

~~~ENDSECTION~~~

!SLIDE bullets
#Alternative Startmöglichkeiten
* WMI und DOM auf Windows
* JNLP (Grafisch)
* Eigenes Script
 - Jenkins verwendet stdin/out zur Kommunikation.

Beispiel:

    @@@ Shell
    ssh slave java -jar ~/bin/slave.jar

~~~SECTION:notes~~~

JNLP: Java Network Launch Protocol
Eigenes Script: slave.jar kommuniziert nicht von selbst mit jenkins

~~~ENDSECTION~~~

