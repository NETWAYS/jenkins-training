!SLIDE bullets noprint
# Why Not Pipeline?
* Pipeline is being hyped as the new big thing
* Visualisation of build processes with Blue Ocean
* Easy separation of steps

!SLIDE smbullets printonly
# Why Not Pipeline?
* Pipeline is being hyped as the new big thing
* Visualisation of build processes with Blue Ocean
* Easy separation of steps

!SLIDE bullets noprint
# Why Not Pipeline?
* Still under development
* Plugins often problematic:
 - Not all Plugins are supported
 - Build in Docker broken
 - Other (e.g. git) have limited use
* Sometimes not much more than a wrapper

!SLIDE smbullets printonly
# Why Not Pipeline?
* Still under development
* Plugins often problematic:
 - Not all Plugins are supported
 - Build in Docker broken
 - Other (e.g. git) have limited use
* Sometimes not much more than a wrapper

!SLIDE bullets noprint
# Why Not Pipeline?
* Pipeline can be used to run other jobs:
  - Easy to use
  - Reduced visualization

    @@@ sh
    pipeline {
      agent any
      stages {
        stage ("Prepare") { steps {
          build 'Preperation Job'
        }}
        stage ("Build") { steps {
          build 'Build Job'
		}}
	 }}

!SLIDE smbullets printonly
# Why Not Pipeline?
* Pipeline can be used to run other jobs:
  - Easy to use
  - Reduced visualization

