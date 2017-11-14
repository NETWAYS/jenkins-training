!SLIDE smbullets noprint
# Why Not Use Pipeline?
* Pipeline is being hyped as the new big thing
* Visualisation of build processes with Blue Ocean
* Easy separation of steps

!SLIDE smbullets noprint
# Why Not Use Pipeline?
* Still under development
* Plugins often problematic:
 - Not all Plugins are supported
 - Build in Docker broken
 - Other (e.g. git) have limited use
* Sometimes not much more than a wrapper

!SLIDE smbullets noprint
# Why Not Use Pipeline?
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
