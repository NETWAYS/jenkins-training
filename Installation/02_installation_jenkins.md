!SLIDE bullets noprint
# Installation
* Java (JDK > 1.7)
* Optional: Tomcat, Glassfish, ...
* Two common ways
 - Package
 - Container + jenkins.war

~~~SECTION:notes~~~
Tomcat wird nur gebaucht wenn man es manuel startet
~~~ENDSECTION~~~

!SLIDE smbullets printonly
# Installation
* Java (JDK > 1.7)
* Optional: Tomcat, Glassfish, ...
* Two common ways
 - Package
 - Container + jenkins.war

!SLIDE
# Installation
Jenkins 2.7.2 package ready to install

* `/home/training/jenkins_2.7.2_all.deb`
* `$ sudo dpkg -i jenkins_2.7.2_all.deb`

!SLIDE
# Starting Jenkins
Start via systemctl

    @@@ shell
    $ sudo systemctl start jenkins

!SLIDE
# Jenkins is now running
By default Jenkins runs on port 8080

    @@@ shell
    http://192.168.56.101:8080

!SLIDE smbullets small
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Setting Up Jenkins
* Objective:
 * Follow the Installation Instructions
* Steps:
 * Find the setup password and enter it
 * Install the suggested plugins
 * Wait for the installation to finish
 * Create an initial user
 * Remember the credentials, all fields need to be filled out


!SLIDE supplemental exercises
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Setting Up Jenkins

## Objective:

****

* Follow the Installation Instructions

## Steps:

****

* Find the setup password and enter it
* Install the suggested plugins
* Wait for the installation to finish
* Create an initial user
* Remember the credentials, all fields need to be filled out

!SLIDE supplemental solutions
# Lab ~~~SECTION:MAJOR~~~.~~~SECTION:MINOR~~~: Proposed Solution

****

## Setting Up Jenkins

****

## Finding The Password

  # sudo cat /var/lib/jenkins/secrets/initialAdminPassword

## Install The Suggested Plugins

<center><img src="./_img/install_suggested_plugins.png"/><center>

~~~PAGEBREAK~~~

## Create An Initial User

<center><img src="./_img/create_user_jenkins.png"/><center>
