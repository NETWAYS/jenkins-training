!SLIDE bullets noprint
# Creating Process
* Single step jobs have limited usabilty
* Jobs can be chained together using conditions
* Allows to represent a multi-step proccess


!SLIDE smbullets small
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Automate The Package Building Proccess
* Objective:
 * Follow up your project with a job that builds a package for it
* Steps:
 * Extract the `suchmaschine_build_files.tar` archive


!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Automate The Package Building Proccess

## Objective:

****

* Automate The Package Building Process

## Steps:

****

* Extract the `suchmaschine_build_files.tar` archive

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## Automate The Package Building Proccess

****

## Extract the `suchmaschine_build_files.tar` archive


# Pakete bauen
* `suchmaschine_build_files.tar` Create example project
* Create job:
  - Clone repository
  - Extract tar archibe
  - Run `debuild --no-tgz-check`

~~~SECTION:notes~~~
tar xvf $name.tar

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Build package
* `suchmaschine_build_files.tar` Create example project
* Create job:
  - Clone repository
  - Extract tar archibe
  - Run `debuild --no-tgz-check`

~~~SECTION:notes~~~
import key gpg --import something.asc
~~~ENDSECTION~~~

!SLIDE bullets noprint
#Chaining
* In our example project `Post-Build Action`:
  - 'Build other projects'
  - Enter an other project

~~~SECTION:notes~~~
Schlägt fehl wegen mangelnder files

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Chaining
* In our example project `Post-Build Action`:
  - 'Build other projects'
  - Enter an other project

!SLIDE bullets noprint
#Access Control
* Missing access control?
* `Authorize Project` Plugin
  - `Conifgure Jenkins`
  - `Global Security`  
  - `Access Control for Builds`
  - `Run as User who Triggered Build`

~~~SECTION:notes~~~
Reines Sicherheits Feature.
Der user unter dem ein Build läuft wird nun beim start des builds und nicht beim
configurieren festgelegt

Daran denken das Jenkins selber entpsrechende Rechte braucht um etwa den user
zu wechseln

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Access Control
* Missing access control?
* `Authorize Project` Plugin
  - `Conifgure Jenkins`
  - `Global Security`  
  - `Access Control for Builds`
  - `Run as User who Triggere Build`

!SLIDE bullets noprint
#Chaining
* `Clone Workspace SCM Plug-in`
* `Multiple SCMs plugin`

~~~SECTION:notes~~~
Im 1. job als post built action archivieren, im 2. job als scm holen
~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Chaining^
* `Clone Workspace SCM Plug-in`
* `Multiple SCMs plugin`

!SLIDE bullets noprint
#Complex build chains
* `conditional-buildstep` Plugin
* Build steps executed on bool conditions

!SLIDE smbullets printonly
#Komplexe Ketten
* `conditional-buildstep` Plugin
* Build steps executed on bool conditions
