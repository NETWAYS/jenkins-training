!SLIDE center
#Was wir schon haben
<img src="./_img/Jenkins Server Single.svg" alt="Single Server"/>

~~~SECTION:notes~~~

Eine volle Jenkins Installation

~~~ENDSECTION~~~

!SLIDE center
#Was wir wollen
<img src="./_img/Jenkins Server Multi.svg" alt="Multi Server"/>

~~~SECTION:notes~~~

Volles Jenkins nur auf Master.
Container (Webserver) nur auf Master.
Agents werden vom master via ssh erstellt und gestartet.
Kommunikation via tcp/ip.

~~~ENDSECTION~~~
