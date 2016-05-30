!SLIDE bullets incremental
#Die Schulungsnotebooks
Verwendungszwecke:

* Verfolgen der Schulungsunterlagen
* Ausführen der virtuellen Maschinen

!SLIDE bullets incremental
#Virtualbox
* Virtualbox starten
[Bild von virtualbox]
* 'jenkins-master' starten

~~~SECTION:notes~~~

TODO: Wie Virtualbox starten?
TODO: Bild von virtualbox mit den 2 maschinen

~~~ENDSECTION~~~

!SLIDE incremental
#jenkins-master
Entweder im VirtualBox-Fenster arbeiten . . .  
. . . oder per SSH auf die Maschine verbinden

    @@@ sh
    ssh jenkins@171.16.32.10
    Passwort: icinga

~~~SECTION:notes~~~

TODO: Richtige Daten eintragen
Wer im Fenster arbeiten möchte braucht auch jenkins:icinga

~~~ENDSECTION~~~

!SLIDE bullets
#root werden
* Der Benutzer 'jenkins' hat geringe Berechtigungen
  - Wir brauchen ihn aber später noch
* 'root' hat volle Kontrolle über die Box

How to?

    @@@ sh
    sudo -i
    Passwort: icinga

