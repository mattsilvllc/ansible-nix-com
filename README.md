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