!SLIDE subsection
#~~~SECTION:MAJOR~~~ Credentials

!SLIDE bullets noprint
# Crendentials have ...
* ... a domain (Group),
* ... a scope (Visibility),
* ... and a type (Name+Password, Certificate, etc.)

~~~SECTION:notes~~~

Besser Erklären?
Domains zur Übersicht, keine neue Erstellen
Scope: System?
Gleich die Credentials eintragen lassen

~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Crendentials have ...
* ... a domain (Group),
* ... a scope (Visibility),
* ... and a type (Name+Password, Certificate, etc.)

!SLIDE smbullets small
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Adding Credentials
* Objective:
 * Add a set of Credentials in the web interface
 * Copy the masters SSH key over to the slave
* Steps:
 * Navigate to the `Credentials` page
 * Add an SSH key to the jenkins user
 * Copy the key over to the agents maschine

!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Adding Credentials

## Objective:

****

* Add a set of Credentials in the web interface
* Copy the masters SSH key over to the slave

## Steps:

****

* Navigate to the `Credentials` page
* Add an SSH key to the jenkins user
* Copy the key over to the agents maschine

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## Adding Credentials

****

## Navigate to the `Credentials` Page

  [TODO IMAGE]

## Add an SSH key to the jenkins user
  
  [TODO]
 - Kind: 'SSH Usermane with private key'
 - Username: `jenkins`
 - `Private Key`: `From the Jenkins master ~/.ssh`
 - ID and Description can be ignored safely

## Copy the key over to the agents maschine

 # ssh-copy-id TODO 192.168.56.102

