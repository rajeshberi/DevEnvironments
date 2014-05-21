Systers Development Environments
================================

This readme file details all Systers development environments for GSoC and open source projects. 

# Project Specific Development Environment
All projects will have the following environment setup unless otherwise specified.

OS Ubuntu
Web Server - Apache
Software/Application Framework - Python/Django (Ushahidi has platform and PHP)
Database - PostgreSQL (Ushahidi has MySQL)
MacOSX, XCode (for iOS developers)

# Server Sotware Version Details
Ubuntu 14.04 LTS (GNU/Linux 3.13.0-24-generic i686)
Apache 2.4.7
Ruby/Rails 2.1.2p95 
GEM 2.2.2
Phython/Django 2.7.6
NodeJS 0.10.25
NPM 1.3.10
MySQL 14.14
PostgreSQL 9.3.4
Git 1.9.1



# Setup

1. Install VirtualBox by going to their [download
page](https://www.virtualbox.org/wiki/Downloads).

2. Install Vagrant by going to their [download page](http://www.vagrantup.com/downloads.html).

A [Vagrant](http://vagrantup.com/) file used for deploying an Ubuntu based development environments. Eeach VM is setup as the development instance of each server. If you need more help installing Vagrant, please take a look at [their
installation documentation](http://docs.vagrantup.com/v2/installation/).



# Using Vagrant

The Vagrantfile is setup to automatically download a VM image that already has the project configured and already deployed. Make sure you cd into one of the environments before running the commands below.

    `gem install vagrant`


## Starting a VM

    vagrant up

**NOTE: If you get an error that a port is currently being used, open up the Vagrantfile and change the port to something else (the second port number listed in the file).**

## Accessing the VM

    vagrant ssh

The initial login will be as the `vagrant` user. If you need root privileges just type `sudo su -`. 

Any files that reside in the directory which contains the Vagrantfile will show up inside of the VM as `/vagrant` so that you are free to edit files from your workstation outside the VM if you want.

## Shutting down the VM

    vagrant halt

## Deleting the VM and starting fresh

**NOTE: This will delete any files on the VM itself. Please be careful!**

    vagrant destroy
    vagrant up


