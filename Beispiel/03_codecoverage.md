!SLIDE subsection
# ~~~SECTION:MINOR~~~ Code Qualität überprüfen

!SLIDE smbullets incremental
#Vorbereitung
* Plugin installieren:
 - Violations

~~~SECTION:notes~~~

TODO: Corbetura mit nosexcoverage

~~~ENDSECTION~~~

!SLIDE smbullets incremental
#Den Job editieren
* Auf den Job klicken
* `Configure`
* Unter `Post-build Actions` -> `Report Violations`
* pylint: `**/.pylint.out`
<img src="./_img/Violations.png" alt="violations" />

~~~SECTION:notes~~~

Keine Leerzeichen im Namen da sonst virtualenv spinnt.  
Auch Optionen durchgehen und kurz ansprechen. (?) Erklären eig. alles  
Advanced Options: Upstream und Downstream werden später erklärt.  
Git: Alles lassen wie es ist.  
Build triggers: Später  

~~~ENDSECTION~~~

!SLIDE code noprint
#Execute Shell

  PYENV_HOME=$WORKSPACE/.venv/    
  if [ -d $PYENV_HOME ]; then
      rm -rf $PYENV_HOME
  fi  
  virtualenv --no-site-packages $PYENV_HOME
  source $PYENV_HOME/bin/activate
  pip install --quiet $WORKSPACE/

~~~SECTION:notes~~~

$WORKSPACE: Jenkins env  
Klick 'See the list of available environment variables' unter execute shell  

~~~ENDSECTION~~~
