!SLIDE subsection
#~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~ Projekt erstellen

!SLIDE bullets 
#Vorbereitung
* Plugin installieren:
 - Git plugin
* Build tools installieren:
 - Python 2.7
 - Pip
 - virtualenv
* Credentials eintragen
 - In unserem Fall nicht nötig

~~~SECTION:notes~~~

Build tools sind schon vorinstalliert.

~~~ENDSECTION~~~

!SLIDE bullets 
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

!SLIDE code noprint
#Execute Shell

    @@@ sh
    PYENV_HOME=$WORKSPACE/.venv/    
    if [ -d $PYENV_HOME ]; then
        rm -rf $PYENV_HOME
    fi  
    virtualenv --no-site-packages $PYENV_HOME
    . $PYENV_HOME/bin/activate
    pip install $WORKSPACE/

~~~SECTION:notes~~~

$WORKSPACE: Jenkins env  
Klick 'See the list of available environment variables' unter execute shell  

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

