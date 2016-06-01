!SLIDE bullets 
#Die Schulungsnotebooks
Verwendungszwecke:

* Verfolgen der Schulungsunterlagen
* Ausführen der virtuellen Maschinen

!SLIDE bullets 
#Virtualbox
* Virtualbox starten
[Bild von virtualbox]
* 'jenkins-master' starten

~~~SECTION:notes~~~

TODO: Wie Virtualbox starten?
TODO: Bild von virtualbox mit den 2 maschinen

~~~ENDSECTION~~~

!SLIDE 
#jenkins-master
Entweder im VirtualBox-Fenster arbeiten . . .  
. . . oder per SSH auf die Maschine verbinden

    @@@ sh
    ssh jenkins-master
    Passwort: netways

~~~SECTION:notes~~~

TODO: Richtige Daten eintragen
Wer im Fenster arbeiten möchte braucht auch training:netways

~~~ENDSECTION~~~

!SLIDE bullets
#root werden
* Der Benutzer 'jenkins' hat geringe Berechtigungen
  - Wir brauchen ihn aber später noch
* 'root' hat volle Kontrolle über die Box

How to?

    @@@ sh
    sudo -i

~~~SECTION:notes~~~

Passwordless erklären

~~~ENDSECTION~~~
