Nutritionix LAMP dev setup
============================

This set of ansible YAML files in cooperation with vagrant will help configure a base `.box` image we can distribute
to developers who want to help on the nutritionix stack. Once a box has been bootstrapped we will export the file and
upload to amazon S3 so it can be easily booted up on any OS. Allowing for cleaner, more consistant way of developing.
Any modifications to the base operating system like packages, or requirements for development should be put into this
project and new `.box` image should be distributed to the cloud and everyone should reinstall their machines by running
`vagrant up`.

#### Base installation

```shell
vagrant up
```

#### Bootstrap an existing vagrant box

```shell
#### from within the vagrant files directory
vagrant provision
```

The `Vagrantfile` is configured to mount one directory up from the directory you cloned this project into. It mounts iselft to `/home/vagrant/www` within the virtual machine. Any files in the mounted directory will be accessible within the virtual machine and apache is configured to serve `/home/vagrant/www`.

Vagrant is attached to LOCAL IP `192.168.33.10` and apache is attached to port 80.