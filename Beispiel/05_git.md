!SLIDE bullets
#Lokaler Git Server

Für die folgenden Aufgaben benötigen wir einen git-server.

Wie das im Detail funktioniert wird in der git-Schulung erklärt.

!SLIDE
# SSH Key Erstellen

Einen ssh key für den jenkins-Benutzer erstellen

    @@@ Sh
    $ ssh-keygen -f ~/.ssh/id_rsa


!SLIDE bullets
# Git User + SSH key

Git braucht einen eigenen Benutzer und ein `.ssh` Verzeichnis

    @@@ Sh
    $ adduser git
    $ su git -c 'mkdir /home/git/.ssh'
    $ cp /home/jenkins/.ssh/id_rsa.pub \
        /home/git/.ssh/authorized_keys

### Verbindungstest

    @@@ Sh
    ssh git@localhost

!SLIDE 
#Repository
### Repository anlegen

    @@@ Sh
    $ mkdir -p /opt/git/suchmaschine
    $ git --bare init /opt/git/suchmaschine/

### Rechte anpassen

    @@@ Sh
    $ chown -R git:git /opt/git

!SLIDE
# Repository
### Repository hinzufügen

    @@@ Sh
    $ tar xvzf suchmaschine.tar.gz
    $ cd suchmaschine
    $ git remote add origin \
      git@localhost:/opt/git/suchmaschine
    $ git fetch

### Commit pushen

    @@@ Sh
    $ git push --set-upstream origin master

