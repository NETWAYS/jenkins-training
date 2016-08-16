!SLIDE noprint
# What A Bad Result
The result was not to our liking.

But we don't want to push the build button again

!SLIDE bullets noprint
# Triggered Builds
* Triggered Builds allow Jenkins to start a build without our help
* Greatly decreases the required interaction

!SLIDE smbullets printonly
# Triggered Builds
* Triggered Builds allow Jenkins to start a build without our help
* Greatly decreases the required interaction

!SLIDE bullets noprint
# Automatic Builds (Trigger)
* `Build after other projects are built`
  - Allows to chain builds
* `Build periodically`
  - Starts the job following a cron-like schedule
* `Poll SCM`
  - Periodically polls a SCM and starts the build when there are changes

~~~SECTION:notes~~~

Schedule TODO: Irgendetwas das nicht so lange dauert wie der nächste Abschnitt
damit der build fertig ist wenn man dazu zurückkehrt.

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Automatic Builds (Trigger)
* `Build after other projects are built`
  - Allows to chain builds
* `Build periodically`
  - Starts the job following a cron-like schedule
* `Poll SCM`
  - Periodically polls a SCM and starts the build when there are changes

!SLIDE bullets noprint
# Adding A Trigger
* `Poll SCM`
* `Schedule`:
 - `H/1 * * * *`
 - 'Every Minute'

!SLIDE smbullets printonly
# Adding A Trigger
* `Poll SCM`
* `Schedule`:
 - `H/1 * * * *`
 - 'Every Minute'

!SLIDE noprint
# Fixing the Project

    @@@ Sh
    $ git config --global user.email "$some_mail"
    $ git config --global user.name "$some_name"
    git commit -a
    # Enter some commit message
    git push

