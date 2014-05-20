Systers Development Environments
================================

This readme file details all Systers development environments for GSoC and open source projects. 

A [Vagrant](http://vagrantup.com/) file used for deploying an Ubuntu based development environments. Eeach VM is setup as the development instance of each server.

# Setup

1. Install VirtualBox by going to their [download
page](https://www.virtualbox.org/wiki/Downloads).

2. Install Vagrant

    `gem install vagrant`

If you need more help installing Vagrant, please take a look at [their
installation documentation](http://docs.vagrantup.com/v2/installation/).

# Using Vagrant

The Vagrantfile is setup to automatically download a VM image that already has
the Systers mailman configured and already deployed. Make sure you cd into one
of the environments before running the commands below.

## Starting a VM

    vagrant up

**NOTE: If you get an error that a port is currently being used, open up the
Vagrantfile and change the port to something else (the second port number listed
in the file).**

## Accessing the VM

    vagrant ssh

The initial login will be as the `vagrant` user. If you need root privileges
just type `sudo su -`. 

Any files that reside in the directory which contains the Vagrantfile will show
up inside of the VM as `/vagrant` so that you are free to edit files from your
workstation outside the VM if you want.

## Shutting down the VM

    vagrant halt

## Deleting the VM and starting fresh

**NOTE: This will delete any files on the VM itself. Please be careful!**

    vagrant destroy
    vagrant up
    
http://localhost:8080/systers-autotest-dev](http://localhost:8080/systers-autotest-dev)
in your browser.

