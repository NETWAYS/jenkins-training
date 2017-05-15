!SLIDE bullets noprint
# Hello Jenkins!

* TODO: Rework this introduction
* `New Item`: Entry point for job creation
* Choose a name and select 'Freestyle Project'
* `Build` -> `Execute Shell`

## Code:

    @@@ sh
    echo "Hello Jenkins"
    exit 0 	  				 	 	 	   	 	  	   		  	 

~~~SECTION:notes~~~

Am Beamer Zeigen

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Job Creation

* `New Item`: Entry point for job creation
* Choose a name and select 'Freestyle Project'
* `Build` -> `Execute Shell`

## Code:

    @@@ sh
    echo "Hello Jenkins"
    exit 0

###TODO: Explain job types here, after explain exit codes
See https://wiki.jenkins-ci.org/pages/viewpage.action?pageId=74876543

!SLIDE smbullets small
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Creating Your First Job
* Objective:
  * Create a Jenkins Job
* Steps:
  * Create a 'Freestyle Project'
  * Add a 'Execute shell'-build step
  * Start the Job and check its output

!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Creating Your First Job

## Objective:

****

* Create a Jenkins job

## Steps:

****

* Create a 'Freestyle Project'
* Add a 'Execute shell'-build step
* Start the Job and check its output

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## Create a Jenkins job

****

## Create a 'Freesyle Project'

<img src="./_img/create_build.png" style="width:600px" />
<img src="./_img/create_build2.png" style="width:600px" />

~~~PAGEBREAK~~~

## Add a 'Execute shell'-build step
<img src="./_img/create_build3.png" style="width:600px" />

Enter:

    @@@ shell
	echo "Hello, Jenkins!"

## Start the Job and check its output
<img src="./_img/create_build4.png" style="width:600px" />
<img src="./_img/create_build5.png" style="width:600px" />

!SLIDE center noprint
#Job Status Page
<img src="./_img/overview_blank.png" />

!SLIDE printonly
#Job Status Page
<center><img src="./_img/overview_blank.png" style="width:600px"/></center>

!SLIDE bullets small noprint
# Job Status Page
* Changes  
Can show a change log (requires an add-on)
* Workspace  
Contains files used and created by a Build

> Note: No guarantee for files in the workspace to persist or be
> cleaned up after a build (There's Plugins for that)

* Build History  
Past Builds, number can be configured.
Contains more detailed state and progress information

~~~SECTION:notes~~~

Wenn der Job etwa auf einem anderen Server gebaut wird als vorher fehlt der
Workspace. (shared workspace möglich)
Wenn man sich nicht darum gekümmert hat keine wichtigen datein im workspace
haben.
Vergangene builds behalten auch die Ergebnise, nicht nur logs

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Job Status Page
* Changes  
Can show a change log (requires an add-on)
* Workspace  
Contains files used and created by a Build

> Note: No guarantee for files in the workspace to persist or be
> cleaned up after a build (There's Plugins for that)

* Build History  
Past Builds, number can be configured.
Contains more detailed state and progress information
