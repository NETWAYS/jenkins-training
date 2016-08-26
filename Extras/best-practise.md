!SLIDE subsection
#~~~SECTION:MAJOR~~~ Best Practise

!SLIDE bullets noprint
#Backups, Backups, Backups
* Use SCM to maintain your configuration
* Tags for successors
* Test in Branches

!SLIDE smbullets printonly
#Backups, Backups, Backups
* Use SCM to maintain your configuration
* Tags for successors
* Test in Branches

!SLIDE smbullets
#What to backup?

* `$JENKINS_HOME/*.xml`
* `$JENKINS_HOME/jobs/*/*.xml`
* `$JENKINS_HOME/nodes/*`
* `$JENKINS_HOME/plugins/*.jpi`
* `$JENKINS_HOME/users/*`

* .gitignore may help

!SLIDE smbullets
# Test machine
* Easier testing on dediacted machines
  - Also on different Hardware
* Commit $JENKINS\_HOME to git
  - Only included config that you really need
  - Don't commit artefacts, logs
  - Test agents could be build with docker
  - Just merge and go productive

!SLIDE bullets  noprint
#Granularity: Keep things simple
* Use dedicated build steps:
  - Reusing parts
  - Smaller parts to debug
  - Get back running error prone jobs

* Workflow/Pipeline Plugin

!SLIDE bullets  noprint
#Granularity: Keep things simple
* Multiple teams - multiple masters
  - Loadbalancing
  - Less plugin bloat
* Different projects on different servers

!SLIDE bullets noprint
#To be uniform
* Easy replacement of uniform agents
* Same tools, same platform
  - Same Dockerfile
* Best Case: Agent provision via Foreman/Ansible etc.

~~~SECTION:notes~~~
Auf diese Art können unter Last oder bei Ausfall einfach neu Agenten
hinzugefügt werden. Auch skalierbar
Auf Foreman, Ansible Schulung hinweisen.
~~~ENDSECTION~~~

!SLIDE smbullets printonly
#Granularity: Keep things simple
* Use dedicated build steps:
  - Reusing parts
  - Smaller parts to debug
  - Get back running error prone jobs

* Workflow/Pipeline Plugin

!SLIDE smbullets printonly
#Granularity: Keep things simple
* Multiple teams - multiple masters
  - Loadbalancing
  - Less plugin bloat
* Different projects on different servers

!SLIDE smbullets printonly
#To be uniform
* Easy replacement of uniform agents
* Same tools, same platform
  - Same Dockerfile
* Best Case: Agent provision via Foreman/Ansible etc.
