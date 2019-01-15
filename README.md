# vagrant-ubuntu-docker-ru
Vagrant box with docker for ru users

[Download from Vagrantip.com](https://app.vagrantup.com/timmson/boxes/ubuntu-docker-ru)

## Build
1. [Install Vagrant](https://www.vagrantup.com/downloads.html) (if virtual)
2. [Install VirtualBox](https://www.virtualbox.org/wiki/Downloads) (or any other)
3. [Install Git](https://git-scm.com/book/en/v2/Getting-Started-Installing-Git)
4. Clone and run
```
git clone https://github.com/timmson/dev-server.git
cd dev-server
vagrant up
```

## Appications
* [Jetbrains YouTrack](http://localhost:8180)
* [Gitlab](http://localhost:8280)
* [Mattermost](http://localhost:8380)
* [Seafile](http://localhost:8480)
* [Paperless](http://localhost:8580)

## Features
* Based on Ubuntu 18.04 x64
* Europe/Moscow timezone
* Apport is off
* "Colored" bash
* Ansible from ppa:ansible/ansible
* Docker/docker-Compose from download.docker.com 
