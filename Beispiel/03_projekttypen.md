!SLIDE subsection
#~~~SECTION:MAJOR~~~ Project types

!SLIDE center noprint
# Many different types exist

<img src="./_img/project_types_many.png" alt="Default Projekte + einige Plugins" />

~~~SECTION:notes~~~

(Auf new Project klicken um Typen zu zeigen)

~~~ENDSECTION~~~

!SLIDE bullets noprint
# Freestyle
* Most simple kind of Project
* Simple Process management possible through chaining

~~~SECTION:notes~~~

Nachteil: Unübersichtlich
Wir verwenden Freestyle Projekte weil es so weniger Optionen zu erklären gibt
TODO: Extra Teil über pipeline projekte

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Freestyle
* Most simple kind of Project
* Simple Process management possible through chaining

!SLIDE bullets noprint
# Multi-configuration project
<img src="./_img/multi_conf_icinga.png" align="right"/>
* Useful for jobs with many parameters
* Axes allow starting many builds with preconfigured parameters at the same time
* Used in the Icinga project to run Builds on on all Architecture-OS combinations

!SLIDE smbullets printonly
# Multi-configuration project
<img src="./_img/multi_conf_icinga.png" align="right"/>
* Useful for jobs with many parameters
* Axes allow starting many builds with preconfigured parameters at the same time
* Used in the Icinga project to run Builds on on all Architecture-OS combinations

!SLIDE bullets noprint
# External Job
* Use Jenkins to monitor program execution
* Useful for process management
* Not part of this Training

!SLIDE smbullets printonly
# External Job
* Use Jenkins to monitor program execution
* Useful for process management
* Not part of this Training

!SLIDE bullets noprint
# Pipeline/Multi-branch Pipeline
* Once knows as 'Workflow'
* Uses a script language to allow extremely sophisticated processes
* Can be integrated with 'Blue Ocean'

~~~SECTION:notes~~~

Ist ein Extra Thema, kann bei Intresse und genug Zeit noch nachgeschoben werden

~~~ENDSECTION~~~

!SLIDE bullets printonly
# Pipeline/Multi-branch Pipeline
* Once knows as 'Workflow'
* Uses a script language to allow extremely sophisticated processes
* Can be integrated with 'Blue Ocean'
