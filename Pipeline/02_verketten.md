!SLIDE bullets noprint
# Creating Process
* Single step jobs have limited usabilty
* Jobs can be chained together using conditions
* Allows to represent a multi-step proccess

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
