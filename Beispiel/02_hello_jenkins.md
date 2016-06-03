!SLIDE
#Hello, Jenkins!

!SLIDE bullets noprint
#Einen neuen Job erstellen

* Auf `New Item` klicken
* Name eingeben und Freestyle Projekt auswählen
* `Build` -> `Execute Shell`

## Code:

    @@@ sh
    echo "Hello Jenkins"
    exit 0 	  				 	 	 	   	 	  	   		  	 

!SLIDE smbullets printonly
#Einen neuen Job erstellen

* Auf `New Item` klicken
* Name eingeben und Freestyle Projekt auswählen
* `Build` -> `Execute Shell`

## Code:

    @@@ sh
    echo "Hello Jenkins"
    exit 0 	  				 	 	 	   	 	  	   		  	 


!SLIDE center noprint
#Die Statusseite
<img src="./_img/overview_blank.png" />

!SLIDE center printonly
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
#Die Statusseite
* Changes  
Kann Changelog anzeigen (muss eingerichtet werden)
* Workspace  
Enthält Dateien vom build gebraucht und erstellt werden

> Achtung: Keine Garantie das Datein im Workspace erhalten bleiben.
> Daten werden auch nicht aufgeräumt (Plugin dafür existiert)

* Build History  
Vergangene Builds, Anzahl konfigurierbar
Enthält genauere Status und Ablaufsinformationen

~~~SECTION:notes~~~

Wenn der Job etwa auf einem anderen Server gebaut wird als vorher fehlt der
Workspace. (shared workspace möglich)
Wenn man sich nicht darum gekümmert hat keine wichtigen datein im workspace
haben.
Vergangene builds behalten auch die Ergebnise, nicht nur logs

~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Die Statusseite
* Changes  
Kann Changelog anzeigen (muss eingerichtet werden)
* Workspace  
Enthält Dateien vom build gebraucht und erstellt werden

> Achtung: Keine Garantie das Datein im Workspace erhalten bleiben.
> Daten werden auch nicht aufgeräumt (Plugin dafür existiert)

* Build History  
Vergangene Builds, Anzahl konfigurierbar
Enthält genauere Status und Ablaufsinformationen
