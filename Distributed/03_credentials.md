!SLIDE subsection
#~~~SECTION:MAJOR~~~ Credentials

!SLIDE bullets noprint
#Credentials
* Not used by a user but Jenkins itself
* Jenkins has its own 'password-manager'
* Credentials are used in various places e.g:
  - Authenticating with a Git server
  - Bindings (withing jobs)
  - Controlling Agents with SSH

!SLIDE smbullets printonly
#Credentials
* Not used by a user but Jenkins itself
* Jenkins has its own 'password-manager'
* Credentials are used in various places e.g:
  - Authenticating with a Git server
  - Bindings (withing jobs)
  - Controlling Agents with SSH

!SLIDE smbullets small
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Adding Credentials
* Objective:
 * Allow the jenkins user to ssh' into the Agent machine
* Steps:
 * Navigate to the `Credentials` page
 * Add an SSH key to the jenkins user
 * Copy the key over to the agents machine

!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Adding Credentials

## Objective:

****

* Allow the jenkins user to ssh' into the Agent machine

## Steps:

****

* Navigate to the `Credentials` page
* Add an SSH key to the jenkins user
* Copy the key over to the agents machine

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## Allow the jenkins user to ssh' into the Agent machine

****

## Navigate to the `Credentials` Page

* Click the `Credentials` link in the leftside menu

## Add an SSH key to the jenkins user

<img src="./_img/add_credentials.png" style="width:600px" />

* ID will be autofilled

## Copy the key over to the agents machine

    @@@ Sh
	sudo ssh-copy-id -i /var/lib/jenkins/.ssh/id_rsa.pub jenkins@192.168.56.111
    Password? "jenkins"
