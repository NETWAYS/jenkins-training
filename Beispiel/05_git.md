!SLIDE smbullets noprint
# About Git
* Git will be used in the course of this training, but it will not be explained in detail.  
* If you are interested in learning more about Git: NETWAYS also offers Git training

!SLIDE bullets noprint
# Using The Local Git Server
* `jenkins-master` has a git server running using `/opt/git`
* The user 'git' already has training@jenkins-master in its authorized\_keys
* A repository for our next project already exists
~~~SECTION:notes~~~

Alles Themen die im Git training vorkommen

~~~ENDSECTION~~~

!SLIDE bullets noprint
# Using The Local Git Server
* There is one thing we still need to do:

    @@@ Shell
	sudo cp -r /home/training/jenkins-ssh/* /var/lib/jenkins/.ssh
	sudo chown -R jenkins:jenkins /var/lib/jenkins/.ssh

* Why? The Jenkins user didn't exist before the installation but it needs to trust our Git
