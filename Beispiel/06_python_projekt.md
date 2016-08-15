!SLIDE subsection
#~~~SECTION:MAJOR~~~ Projekt erstellen

!SLIDE bullets noprint
#Vorbereitung
* Plugin installieren:
 - Git plugin
* Build tools installieren:
 - Python 2.7
 - Pip
 - virtualenv
* Credentials eintragen
 - jenkins

~~~SECTION:notes~~~

Build tools sind schon vorinstalliert.

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Vorbereitung
* Plugin installieren:
 - Git plugin
* Build tools installieren:
 - Python 2.7
 - Pip
 - virtualenv
* Credentials eintragen
 - In unserem Fall nicht nötig

!SLIDE bullets noprint
#Einen neuen Job erstellen
* Auf `New Item` klicken
* Name eingeben und `Freestyle projekt` auswählen
* `Source Code management`:
 - Git Url: `git@localhost:/opt/git/training.git`
* `Build` -> `Execute Shell`

~~~SECTION:notes~~~

Keine Leerzeichen im Namen da sonst virtualenv spinnt.  
Auch Optionen durchgehen und kurz ansprechen. (?) Erklären eig. alles  
Advanced Options: Upstream und Downstream werden später erklärt.  
Git: Alles lassen wie es ist.  
Build triggers: Später  

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Einen neuen Job erstellen
* Auf `New Item` klicken
* Name eingeben und `Freestyle projekt` auswählen
* `Source Code management`:
 - Git Url: `git@localhost:/opt/git/training.git`
* `Build` -> `Execute Shell`

!SLIDE smbullets printonly
#Einen neuen Job erstellen
* Auf `New Item` klicken
* Name eingeben und `Freestyle projekt` auswählen
* `Source Code management`:
 - Git Url: `git@localhost:/opt/git/training.git`
* `Build` -> `Execute Shell`

!SLIDE code
#Execute Shell

    @@@ sh
    PYENV_HOME="$WORKSPACE"/.venv/
    if [ -d "$PYENV_HOME" ]; then
        rm -rf "$PYENV_HOME"
    fi
    virtualenv --no-site-packages "$PYENV_HOME"
    . "$PYENV_HOME"/bin/activate
    pip install "$WORKSPACE/"

~~~SECTION:notes~~~

"PYENV .. $WORKSPACE" $WORKSPACE erklären, andere vars zeigen  
"if..rm..fi" Geht sicher das nichts von vorherigen builds bleibt  
"virtualenv..HOME" Erstellt isolierte python umgebung
" . ... activate" Wechselt in isollierte umgeben (mit imports erklären)
"pip install" Installiert projekt in virtualenv

~~~ENDSECTION~~~

!SLIDE noprint
#Build it!
<img src="./_img/build_now.png" alt="Build Now!" />

!SLIDE noprint
#Build it!
<img src="./_img/build_running.png" />

~~~SECTION:notes~~~

Live Konsolen output ist zu sehen, interessant zum debuggen


~~~ENDSECTION~~~

