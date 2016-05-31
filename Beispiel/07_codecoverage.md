!SLIDE subsection
#~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~ Metriken generieren

!SLIDE bullets
#Vorbereitung
* Plugin installieren:
 - Violations
 - Cobertura

~~~SECTION:notes~~~

Teilnehmer sollen selbst addons installieren
Kein Neustart erforderlich

~~~ENDSECTION~~~

!SLIDE smbullets incremental
#Den Job editieren
* Auf den Job klicken
* `Configure`
* `Post-build Actions` -> `Report Violations`  
 -> '\*\*/pylint.out'  
<img src="./_img/Violations.png" alt="violations" />
* `Post-build Actions` -> `Publish Cobertura Report`  
 -> '\*\*/covarage.xml'  
<img src="./_img/Cobertura.png" alt="cobertura" />

~~~SECTION:notes~~~

TODO: Erklärung Grenzwerte, Erklärung ** foo

~~~ENDSECTION~~~

!SLIDE small code
#Execute Shell
    @@@ sh
    PYENV_HOME=$WORKSPACE/.venv/    
    if [ -d $PYENV_HOME ]; then
        rm -rf $PYENV_HOME
    fi  
    virtualenv --no-site-packages $PYENV_HOME
    . $PYENV_HOME/bin/activate
    pip install --quiet pylint
    pip install --quiet nosexcover
    pip install $WORKSPACE/
    pylint -f parseable $WORKSPACE | tee pylint.out
    nosetests --with-xcoverage --with-xunit \
      --cover-package=$WORKSPACE --cover-erase

~~~SECTION:notes~~~

$WORKSPACE: Jenkins env  
Klick 'See the list of available environment variables' unter execute shell  

~~~ENDSECTION~~~

!SLIDE noprint
#Das Ergebnis
<img src="./_img/output_bad.png" alt="Schlechtes Ergebnis" />

~~~SECTION:notes~~~

Gute Übersicht über Code Qualität und Testcoverage.  
nosexcoverage zeigt auch die coverage der packages im virtualenv an, sonst
würde nichts zu sehen sein (suchmaschine hat keine tests)

~~~ENDSECTION~~~
