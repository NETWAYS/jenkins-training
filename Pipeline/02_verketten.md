!SLIDE bullets noprint
# Creating a Process
* Single step jobs have limited usabilty
* Jobs can be chained together using conditions
* Allows to represent a multi-step proccess

~~~SECTION:notes~~~
import key gpg --import something.asc
~~~ENDSECTION~~~

!SLIDE bullets noprint
#Chaining
* The Python job now requires the docker job to be build first
* There are multiple ways to model this dependency with Jenkins

~~~SECTION:notes~~~
Schlägt fehl wegen mangelnder files

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Chaining
* The Python job now requires the docker job to be build first
* There are multiple ways to model this dependency with Jenkins

!SLIDE bullets noprint
# Why We Don't Use A Build Trigger
* 'Build after other projects are built' is not a good choice in this case
* Traceability suffers
* Useful for downstream and cleanup jobs

~~~SECTION:notes~~~
Nachverfolgbarkeit von Fehlern leidet
Daher nicht zu empfehlen bei upstream jobs
~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Why We Don't Use A Build Trigger
* 'Build after other projects are built' is not a good choice in this case
* Traceability suffers
* Useful for downstream and cleanup jobs

!SLIDE bullets noprint
#Chaining
* `Clone Workspace SCM Plug-in`
* `Multiple SCMs plugin`

~~~SECTION:notes~~~
Im 1. job als post built action archivieren, im 2. job als scm holen
~~~ENDSECTION~~~

!SLIDE bullets noprint
#Complex build chains
* `conditional-buildstep` Plugin
* Build steps executed on bool conditions

!SLIDE smbullets printonly
#Complex build chains
* `conditional-buildstep` Plugin
* Build steps executed on bool conditions

!SLIDE smbullets small
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Automating The Package Building Process
* Objective:
 * Build a deb package of your project
* Steps:
 * Create a new job that is run after the first
 * Include the `suchmaschine_build_files.tar`
 * Create the package

!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Automating The Package Building Process

## Objective:

****

* Build a deb package of your project

## Steps:

****

* Create a new job that is run after the first
* Include the `suchmaschine_build_files.tar`
* Make sure all required files are in the right place
* Create the package

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## Automating The Package Building Process

****

## Create a new job that is run after the first

* You should be able to create jobs by now
* Add this second job to the first 'Post-Build Actions'

## Include the `suchmaschine_build_files.tar`

* Extract them with `tar xzvf suchmaschine_build_files.tar`
* Either create an additional repository
* Or add them to the first repository

## Make sure all required files are in the right place

* The build files need to be inside the 'suchumaschine' directory
* You need most files from the 'suchmaschine'-project

## Create the package

* `debuild --no-tgz-check -uc -us` should work if everything is in the right place
