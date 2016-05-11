# vagrant-ubuntu64-16.04
Vagrant dev box

## Overview
This vagrant box uses unbuntu 64-bit 16.04 LTS suitable for development work
It contains the following dev tools:
* sublime
* jenv (for java, sbt, scala, ant)
* sdkman (for gradle, grails)
* nvm (for node, npm)
* rvm (for ruby, rails)
* eclipse vX.X.X.X
* intellij vX.X.X.X
* ansible
* docker
* command line tools (yakuake, htop, curl, alien, libaio1)


## Downloading vagrant box
If you're on a slower connection you can copy the latest box from
https://atlas.hashicorp.com/boxcutter/boxes/ubuntu1604-desktop
and make changes to the Vagrantfile to use the downloaded file.


It will mount guest@:/install-buck from host@:~/Downloads.
All the required software will be downloaded to guest@:/install-buck.


## Prerequisites
* Vagrant is installed on the host box
* Ansible is installed on the host box
* proxy is running on the host box if you're using the proxy


## Installation for the first time
1. > vagrant plugin install vagrant-proxyconf
2. > vagrant --provision up [--proxy=true]

## Reload vagrant image after config change
1. > vagrant up
1. > vagrant provision
2. > vagrant reload
