!SLIDE bullets noprint
# Hello Jenkins!

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

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_blank.png" />

!SLIDE printonly
#Die Statusseite
<center><img src="./_img/overview_blank.png" style="width:600px"/></center>

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_overview.png" />

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_changes.png" />

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_workspace.png" />

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_build_now.png" />

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_delete.png" />

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_configure.png" />

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_history.png" />

!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_trend.png" />


!SLIDE bullets small noprint
# The Statuspage
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
# The Status page
* Changes  
Can show a change log (requires an add-on)
* Workspace  
Contains files used and created by a Build

> Note: No guarantee for files in the workspace to persist or be
> cleaned up after a build (There's Plugins for that)

* Build History  
Past Builds, number can be configured.
Contains more detailed state and progress information
