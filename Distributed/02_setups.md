!SLIDE center noprint
# Current State
<img src="./_img/Jenkins_Server_Single.svg" alt="Single Server"/>

~~~SECTION:notes~~~

Eine Installation mit beliebig vielen Executoren

~~~ENDSECTION~~~

!SLIDE printonly
# Current State
<center><img src="./_img/Jenkins_Server_Single.svg" style="width:600" alt="Single Server"/><center>

!SLIDE center noprint
# Simple Agent Setup
<img src="./_img/Jenkins_Server_Multi.svg" alt="Multi Server"/>

~~~SECTION:notes~~~

Volles Jenkins nur auf Master.
Webserver nur auf Master.
Agents werden vom master via ssh autmatisch installiert und gestartet.
Kommunikation via tcp/ip.

~~~ENDSECTION~~~

!SLIDE printonly
# Simple Agent Setup
<center><img src="./_img/Jenkins_Server_Multi.svg" style="width:480;height:267px" alt="Multi Server"/></center>

!SLIDE bullets noprint
# Agents, Nodes, Master?!

* Jenkins(-Master): A full Jenkins installation.
* Agent: Not a full installation, controlled and configured on a master. Can run jobs.
* Node: A Jenkins(-Master) or an agent

!SLIDE smbullets printonly
# Agents, Nodes, Master?!

* Jenkins(-Master): A full Jenkins installation.
* Agent: Not a full installation, controlled and configured on a master. Can run jobs.
* Node: A Jenkins(-Master) or an agent

!SLIDE bullets noprint
# The SSH-Agent
* Master requires SSH-access to the agent-machine
  - Everything else is done by Jenkins
* Required tools (python, virtualenv, ...) need to be installed by the user

~~~SECTION:notes~~~

Tools sind schon vorinstalliert (ausser virtualenv, geplanter fehlschlag)

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# The SSH-Agent
* Master requires SSH-access to the agent-machine
  - Everything else is done by Jenkins
* Required tools (python, virtualenv, ...) need to be installed by the user

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

!SLIDE bullets noprint
# Connecting The Master To Its Agent
* Jenkins has to be able to establish a connection
* With help of the user (eg. JNLP)
* Or letting Jenkins connect (eg. SSH)

!SLIDE smbullets printonly
# Connecting The Master To Its Agent
* Jenkins has to be able to establish a connection
* With help of the user (eg. JNLP)
* Or letting Jenkins connect (eg. SSH)
