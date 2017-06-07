!SLIDE subsection
#~~~SECTION:MAJOR~~~ Groovy Script

!SLIDE bullets noprint
# Groovy Script
Topics in this chapter

* General Groovy Usage
* Possible applications
* Simple Groovy Script Example
* Security Concerns

!SLIDE smbullets printonly
# Groovy Script
Topics in this chapter

* General Groovy usage
* Possible applications
* Simple Groovy script example
* Security concerns


!SLIDE bullets noprint
# General Groovy Usage
* `/script` for web console
* CLI can be used with curl (HTTPS)
* 'Remoting' as an insecure legacy option
* `JENKINS_HOME/init.groovy.d/*.groovy` is run on startup

~~~SECTION:notes~~~
~~~ENDSECTION~~~

!SLIDE smbullets printonly
# General Groovy Usage
The Jenkins script console is accessible in two locations:
* `/script` for web console
* CLI can be used with curl (HTTPS)
* 'Remoting' as an insecure legacy option
* `JENKINS_HOME/init.groovy.d/*.groovy` is run on startup

!SLIDE bullets noprint
# Possible Applications
* Groovy is quite powerful.
* It can also be safely ignored.
* Can be used to make tedious tasks easy...
* ... Or automate Jenkins deployment completly

!SLIDE smbullets printonly
# Possible Applications
* Groovy is quite powerful.
* It can also be safely ignored.
* Can be used to make tedious tasks easy...
* ... Or automate Jenkins deployment completly

!SLIDE bullets noprint
# Security concerns
* Script user can do anything the jenkins user can
* Remoting is a BAD idea
* Disabled by default in newer versions
* Puppet module requires it

!SLIDE smbullets printonly
# Security Concerns
* Script user can do anything the jenkins user can
* Remoting is a bad idea
* Disabled by default in newer versions
* Puppet module requires it

