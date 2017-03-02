# vagrant-modxbughunt
Vagrant VM (with 3 MODX installs defined) for MODX Bug Hunt 2017

# IMPORTANT!

This Vagrant machine expects you to have the following Vagrant plugins installed:

1. Install a Vagrant plugin, [vagrant-hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater) to update your `/etc/hosts` automatically
    ```
	vagrant plugin install vagrant-hostsupdater
	```
1. Install another Vagrant plugin, [vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest) to keep the guest additions automatically up to date:
    ```
	vagrant plugin install vagrant-vbguest
	```
  
If you are running Windows, also install `vagrant-winnfsd`.

# Setup MODX

Checkout your fork of MODX into `modx/web` (and `modx10/web` and `modx20/web` if you want multiple installs)

## Database connection details

Host: localhost
Username: vagrant
Password: testing123

Database names: modxbughunt / modxbughunt10 / modxbughunt20

All databases are populated from `setup/modxbughunt.sql` when the Vagrant machine is populated. So once you've installed MODX, if you dump your database to that file, when you recreate the VM it'll be present.

## URLs

  * http://modxbughunt.local
  * http://modxbughunt10.local
  * http://modxbughunt20.local
