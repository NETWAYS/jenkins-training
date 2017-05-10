!SLIDE smbullets noprint
# Jenkins Job Options
* Job Options fall in one of three categories
  - Meta options: Describe how Jenkins displays and handles jobs
  - Preperation: Actions run before the actual build step
  - Post-build: Are run after the job is finished

~~~SECTION:notes~~~

Beispiele geben!
meta: Disable this project
Preperation: git scm
Post-build: Run another job, publish test results

~~~ENDSECTION~~~

!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Generating Metrics

## Objective:

****

* Use plugins to collect and display metrics

## Steps:

****

* Edit the job to use the plugins
* Update the build step
* Check out your results

~~~SECTION:notes~~~

TODO: Erklärung Grenzwerte, Erklärung ** foo
Ant-style pfade 

"pip --quiet ..." installiert aus dem Netz, output interssiert nicht
"pylint ..." Statische code analyse (anhand output erklären)
"nosetest ..." python unit tests, überprüfen einzelne code teile

Gute Übersicht über Code Qualität und Testcoverage.  
nosexcoverage zeigt auch die coverage der packages im virtualenv an, sonst
würde nichts zu sehen sein (suchmaschine hat keine tests)
Wenn es fehlschlägt, wahrscheinlich wegen Leerzeichen im Projektnamen

~~~ENDSECTION~~~

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## Set up the python build job

****

## Edit the job to use the plugins

* Configure job
* `Post-build Actions` -> `Publish Cobertura Report`  
 -> '\*\*/covarage.xml'  
<img src="./_img/Cobertura.png" alt="cobertura" />
* `Post-build Actions` -> `Report Violations`  
 -> '\*\*/pylint.out'  
<img src="./_img/Violations.png" alt="violations" />

## Update the build step

* Execute Shell:

    @@@ sh
    PYENV_HOME="$WORKSPACE"/.venv/    
    if [ -d "$PYENV_HOME" ]; then
        rm -rf "$PYENV_HOME"
    fi  
    virtualenv --no-site-packages "$PYENV_HOME"
    . "$PYENV_HOME"/bin/activate
    pip install --quiet pylint
    pip install --quiet nosexcover
    pip install "$WORKSPACE/"
    pylint -f parseable "$WORKSPACE" | tee pylint.out
    nosetests --with-xcoverage --with-xunit \
      --cover-package="$WORKSPACE" --cover-erase

## Check out your results
* Run your job
* Got on the jobs detail page

<img src="./_img/output_bad.png" />
