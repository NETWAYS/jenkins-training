!SLIDE
#Too many plugins

Using too many plugins results into dependencies and performance issues.

What can we do?

!SLIDE bullets noprint
#Workflow/Pipeline Plugin
* install 'Pipeline' plugin
  - Aka "Workflow Plugin"
  - Official recommendation to build jobs
  - Very complex

~~~SECTION:notes~~~

Ehemals "Workflow", heisst noch so in älterer Dokumentation
Mit Jenkins 2.0 als zentraler Projekttyp empfohlen

Erklärung nächste Folie

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Workflow/Pipeline Plugin
* install 'Pipeline' plugin
  - Aka "Workflow Plugin"
  - Official recommendation to build jobs
  - Very complex

!SLIDE center
#Workflow/Pipeline Plugin
Create new (Pipeline) project

!SLIDE center
#Pipeline Script
<img src="./_img/pipeline_script.png" style="width:1000px" alt="Pipeline Script?">

~~~SECTION:notes~~~

'Pipeline Syntax' Klicken für Code Generator
Definition per Hand oder aus SCM

~~~ENDSECTION~~~

!SLIDE bullets noprint
#Pipeline Script
* Script language is Groovy
* Included Jenkins api
* 'Pipeline Syntax': Snippet Editor

!SLIDE smbullets printonly
#Pipeline Script
* Script language is Groovy
* Included Jenkins api
* 'Pipeline Syntax': Snippet Editor

!SLIDE bullets noprint
#Pipeline Syntax
* `Stage`
  - Logically distinct part of the execution of any task
* `Node`
  - Contain multiple steps and create workspaces (not permanet)
* `Step`
  - A single part of the sequence

~~~SECTION:notes~~~
Node: Mehrere Steps da Workspace erstellen und löschen ein Schritt ist
~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Pipeline Syntax
* `Stage`
  - Logically distinct part of the execution of any task
* `Node`
  - Contain multiple steps and create workspaces (not permanet)
* `Step`
  - A single part of the sequence

!SLIDE bullets

!SLIDE bullets noprint
#Freestyle to Pipleine
Convert our Python project to Pipeline.

* `Pipeline Syntax`
* `checkout: General SCM`
* Enter configuration
* `Generate Groovy`

!SLIDE smbullets printonly
#Freestyle to Pipeline
Convert our Python project to Pipeline.

* `Pipeline Syntax`
* `checkout: General SCM`
* Enter configuration
* `Generate Groovy`

!SLIDE bullets noprint
#Freestyle to Pipeline
* Enclose checkout with`node { }`
* Optional stages:
  - `stage 'SCM'`
  - The stage is active until a new stage is created

~~~SECTION:notes~~~

`$WORKSPACE` ist nicht mehr vorhanden aber der Job startet _immer_
im worspace (pwd = $WORKSPACE)  
Langsam ausklingen lassen, Extra teil ankündigen

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Freestyle to Pipleine
* Enclose checkout with`node { }`
* Optional stages:
  - `stage 'SCM'`
  - The stage is active until a new stage is created

!SLIDE bullets noprint
#Pipeline as code
* Pipeline scripts are code and should be handled like that:
  - Less tolerant when using templates or wizards
  - Unlimited features
  - Hard to learn
  - Use a SCM to maintain your configuration (`Pipeline Script from SCM`)

~~~SECTION:notes~~~
Für mehr reicht die Zeit nicht, Pipline ist eine Option die für kleine Installationen
overkill ist  
Wenn keine Fragen, dann Security + Best practise
~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Pipeline as code
* Pipeline scripts are code and should be handled like that:
  - Less tolerant when using templates or wizards
  - Unlimited features
  - Hard to learn
  - Use a SCM to maintain your configuration (`Pipeline Script from SCM`)
