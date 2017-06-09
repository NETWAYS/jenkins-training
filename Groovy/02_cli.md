!SLIDE bullets noprint
# Jenkins CLI
* Offers many shortcuts for management
  - `install-plugin`
  - `disable-job`
  - `safe-restart`
* Evaluates Groovy (`groovy`, `groovysh`)
* Used by many provisioning tools

!SLIDE smbullets printonly
# Jenkins CLI
* Offers many shortcuts for management
  - `install-plugin`
  - `disable-job`
  - `safe-restart`
* Evaluates Groovy (`groovy`, `groovysh`)
* Used by many provisioning tools

!SLIDE bullets noprint
# Jenkins CLI Usage

Usage is a bit counterintuitive:

    @@@ Shell
    $ java -jar jenkins-cli.jar [-s URL] command [opts...] args

	# Example:
	$ java -jar jenkins-cli.jar -s localhost:8080 \
	    help --username $USER --password $PASS

* Long options after command.
* Can use `JENKINS_URL` env variable and others to ignore some options.

!SLIDE smbullets printonly
# Jenkins CLI Usage

Usage is a bit counterintuitive:

    @@@ Shell
    $ java -jar jenkins-cli.jar [-s URL] command [opts...] args

	# Example:
	$ java -jar jenkins-cli.jar -s localhost:8080 \
	    help --username $USER --password $PASS

* Long options after command.
* Can use `JENKINS_URL` env variable and others to ignore some options.

!SLIDE bullets noprint
# Jenkins CLI Security
* Authentication via
  - SSH key
  - Username + password
* `Remoting`: Deprecated, but often required option
* Script user has full power over Jenkins

~~~SECTION:notes~~~
remoting is required for script usage
~~~ENDSECTION~~~


!SLIDE bullets noprint
# Jenkins CLI Security
* Authentication via
  - SSH key
  - Username + password
* `Remoting`: Deprecated, but often required option
* Script user has full power over Jenkins
