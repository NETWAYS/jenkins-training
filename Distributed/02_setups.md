# Architecture and Startup

!SLIDE center noprint
# This Is What We Have
<img src="./_img/Jenkins_Server_Single.svg" alt="Single Server"/>

~~~SECTION:notes~~~

Eine Installation mit beliebig vielen Executoren

~~~ENDSECTION~~~

!SLIDE printonly
# This Is What We Have
<center><img src="./_img/Jenkins_Server_Single.svg" style="width:600" alt="Single Server"/><center>

!SLIDE center noprint
# This Is What We Want
<img src="./_img/Jenkins_Server_Multi.svg" alt="Multi Server"/>

~~~SECTION:notes~~~

Volles Jenkins nur auf Master.
Webserver nur auf Master.
Agents werden vom master via ssh autmatisch installiert und gestartet.
Kommunikation via tcp/ip.

~~~ENDSECTION~~~

!SLIDE printonly
# This Is What We Want
<center><img src="./_img/Jenkins_Server_Multi.svg" style="width:480;height:267px" alt="Multi Server"/></center>

!SLIDE bullets noprint
# The SSH-Agent
* Master needs SSH-access to the agents maschine
  - Everything else is done by Jenkins
* Required tool (python, virtualenv, ...) need to be installed by the user

~~~SECTION:notes~~~

Tools sind schon vorinstalliert (ausser virtualenv, geplanter fehlschlag)

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# The SSH-Agent
* Master needs SSH-access to the agents maschine
  - Everything else is done by Jenkins
* Required tool (python, virtualenv, ...) need to be installed by the user

!SLIDE bullets noprint
# Alternative Agents
* WMI and DOM on Windows
* JNLP (graphical)
* Your own script
 - Jenkins uses stdin/out for communication.

~~~SECTION:notes~~~

JNLP: Java Network Launch Protocol
Eigenes Script: slave.jar kommuniziert nicht von selbst mit jenkins

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Alternative Agents
* WMI and DOM on Windows
* JNLP (graphical)
* Your own script
 - Jenkins uses stdin/out for communication.
