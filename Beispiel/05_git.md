!SLIDE
#Exkurs: Git

!SLIDE
#Lokaler Git Server

Für die folgenden Aufgaben benötigen wir einen git-server.

Wie das im Detail funktioniert wird in der git-Schulung erklärt.

!SLIDE
# SSH Key Erstellen

Einen ssh key für den jenkins-Benutzer erstellen

    @@@ Sh
    $ sudo su jenkins -c 'ssh-keygen'


!SLIDE
# Git User + SSH key

Git braucht einen eigenen Benutzer und ein `.ssh` Verzeichnis

    @@@ Sh
    $ sudo adduser git
    $ sudo su git -c 'mkdir /home/git/.ssh'
    $ sudo cp /home/training/.ssh/id_rsa.pub \
          /home/git/.ssh/authorized_keys
    $ sudo su -c "cat /home/training/.ssh/id_rsa.pub \
         >> /home/git/.ssh/authorized_keys"

!SLIDE
# user = training?
Das selbe muss für den user 'training' wiederholt werden.

### Verbindungstest

    @@@ Sh
    ssh git@localhost

~~~SECTION:notes~~~

Einen Satz zu jeder Zeile sagen
Wir brauchen beide ssh keys im git auth keys

~~~ENDSECTION~~~

!SLIDE 
#Repository
### Repository anlegen

    @@@ Sh
    $ sudo mkdir -p /opt/git/suchmaschine.git
    $ sudo git --bare init /opt/git/suchmaschine.git/

### Rechte anpassen

    @@@ Sh
    $ sudo chown -R git:git /opt/git

~~~SECTION:notes~~~

Einen Satz zu jeder Zeile sagen
suchmaschine.git !! .git passt nicht auf die folie

~~~ENDSECTION~~~

!SLIDE
# Repository
### Repository hinzufügen

    @@@ Sh
    $ cd /home/training
    $ tar xvzf suchmaschine.tar.gz
    $ cd suchmaschine
    $ git remote add origin \
      git@localhost:/opt/git/suchmaschine.git
    $ git fetch

### Commit pushen

    @@@ Sh
    $ git push --set-upstream origin master

~~~SECTION:notes~~~

Einen Satz zu jeder Zeile sagen
Der commit wurde schon vorbereitet
sshkey training ist in /git/authrized keys

KAPITEL ÜBERSPRINGEN, CREDENTIALS SIND NÖTIG
DISTRIBUTED CREDENTIALS

~~~ENDSECTION~~~
