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
#What To Backup?

* `$JENKINS_HOME/*.xml`
* `$JENKINS_HOME/jobs/*/*.xml`
* `$JENKINS_HOME/nodes/*`
* `$JENKINS_HOME/plugins/*.jpi`
* `$JENKINS_HOME/users/*`
* gitignore helps

!SLIDE smbullets
# Test Machine
* Easier testing on dedicated machines
  - Also on different Hardware
* Commit $JENKINS\_HOME to git
  - Only included config that you really need
  - Don't commit artifacts or logs
  - Test agents could be build with docker
  - Just merge and go productive

!SLIDE bullets  noprint
#Granularity: Keep Things Simple
* Use dedicated build steps:
  - Reusing parts
  - Smaller parts to debug
  - Get back running error prone jobs

* Workflow/Pipeline Plugin

!SLIDE bullets  noprint
#Granularity: Keep things simple
* Multiple teams - multiple masters
  - Load balancing
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
  - Load balancing
  - Less plugin bloat
* Different projects on different servers

!SLIDE smbullets printonly
#To be uniform
* Easy replacement of uniform agents
* Same tools, same platform
  - Same Dockerfile
* Best Case: Agent provision via Foreman/Ansible etc.
