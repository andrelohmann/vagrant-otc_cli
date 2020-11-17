# vagrant-otc_cli

(c) Andre Lohmann (and others) 2020

## Maintainer Contact
 * Andre Lohmann
   <lohmann.andre (at) gmail (dot) com>

## content

This vagrant machine will install "openstackclient" and "otcextensions" to control an otc (Open Telekom Cloud) tenant by cli.

https://python-otcextensions.readthedocs.io/en/latest/install/pip_install.html

## Prequesites

### VirtualBox

  * Install the latest virtualbox from oracle repositories (https://www.virtualbox.org/wiki/Downloads)
  * If you are on a linux distro, follow the instructions to add the oracle repo
  * Install the latest Oracle VM VirtualBox Extension Pack

### Vagrant

#### cli

  * Install the latest vagrant (https://www.vagrantup.com/downloads.html)

#### plugins

The vagrant machines depends on the following vagrant plugins.

```
vagrant plugin install vagrant-vbguest
```

These plugins should get installed automatically on a "vagrant up", if that fails anyways, please manually install the plugins by entering the commands.

## usage

### upstart

  * Clone the repo and change to the directory
  * copy ansible_vagrant/custom_vars.yml.example to ansible_vagrant/custom_vars.yml
  * customize ansible_vagrant/custom_vars.yml to your needs
  * Run the machine

```
vagrant up
```

### use

Enter the machine.

```
vagrant ssh
```

Run a openstack hello world.

```
openstack --os-cloud otc flavor list
```
