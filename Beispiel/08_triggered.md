!SLIDE noprint
#Unzufrieden?
Das Ergebnis ist nicht gut genug!

Verbesserter Code wird gepushed, Build soll automatisch starten

!SLIDE bullets
#Triggered Builds
* Triggered Builds erlauben es Jenkins selbststädig builds anzustoßen
* Senkt erfordete Interaktion

!SLIDE bullets
#Automatische builds (trigger)
* `Build after other projects are built`
  - Erlaubt Aneinanderreihung von builds
* `Build periodically`
  - Startet Job nach einen Cron-like Plan
* `Poll SCM`
  - Startet Job nur wenn Änderungen im SCM gefunden werden

~~~SECTION:notes~~~

Schedule TODO: Irgendetwas das nicht so lange dauert wie der nächste Abschnitt
damit der build fertig ist wenn man dazu zurückkehrt.

~~~ENDSECTION~~~

!SLIDE bullets
#Trigger hinzufügen
* `Poll SCM`
* `Schedule`:
 - `H/5 * * * *`
 - 'Alle fünf Minuten'

!SLIDE noprint
#Projekt patchen

    @@@ Sh
    $ git config --global user.email "$some_mail"
    $ git config --global user.name "$some_name"
    git commit -a
    # Commit Nachricht eingeben
    git push
    sleep 5m


