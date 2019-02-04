# Drupal VM

This project makes local Drupal test/development environment management quick and easy. It installs the following on an Ubuntu linux VM:

  - Apache
  - PHP
  - MySQL
  - Drush
  - Drupal

It takes 5-10 minutes to build 

## Quick Start Guide

### 1 - Install dependencies (VirtualBox, Vagrant, Ansible)

  1. Download and install [VirtualBox](https://www.virtualbox.org/wiki/Downloads).
  2. Download and install [Vagrant](http://www.vagrantup.com/downloads.html).
  3. Install [Ansible](http://docs.ansible.com/intro_installation.html).

### 2 - Build the Virtual Machine

  1. Download this project and put it wherever you want.
  2. Open Terminal, cd to this directory (containing the `Vagrantfile` and this REAMDE file).
  3. Type in `vagrant up`.

### 3 - Configure your host machine to access the VM.

  1. [Edit your hosts file] adding the line `192.168.88.8  drupal.test` so you can connect to the VM.
  2. Open your browser and access [http://drupal.test/](http://drupal.test/) or http://192.168.88.8

## Notes

  - To shut down the virtual machine, enter `vagrant halt` in the Terminal in the same folder that has the `Vagrantfile`. To destroy it completely (if you want to save a little disk space, or want to rebuild it from scratch with `vagrant up` again), type in `vagrant destroy`.
  - You can change the version of Drupal installed by editing the variables within `vars.yml`.
  - You can either use Drush or Git to download Drupal (either way results in the same thing); see the commented-out Drush download method in `play.yml`.

