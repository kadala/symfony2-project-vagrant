symfony2-project-vagrant
========================

bin : folder with wrapper scripts for easier managemnt and usage of the VM.
puphpet : provisioning for the vagrant box. This folder contains also the yaml file to configure the Vagrant box and its provisioning.

* Website: [http://www.vagrantup.com](http://www.vagrantup.com)
* Source: [https://github.com/mitchellh/vagrant](https://github.com/mitchellh/vagrant)
* IRC: `#vagrant` on Freenode
* Mailing list: [Google Groups](http://groups.google.com/group/vagrant-up)

Symfony 2 Vagrant is a tool for building and distributing development environments.

Vagrant provides the framework and configuration format to create and
manage complete portable development environments. These development
environments can live on your computer or in the cloud, and are portable
between Windows, Mac OS X, and Linux.

Vagrant Install
---------------

```
vagrant init hashicorp/precise32
```

```
vagrant up
```

```
vagrant ssh
```

VM content
----------

The VM is based on the [ubuntu-precise12042-x64-vbox43 box](http://box.puphpet.com/ubuntu-precise12042-x64-vbox43.box) hosted on the puphpet server.

The provioning installs to the box:

* [Mailcatcher](http://mailcatcher.me/): outgoing emails are captured by this tool. Emails can be read by opening the web mail reader 
[http://192.168.56.154:1080](http://192.168.56.154:1080).
* Apache 2.2.22
* PHP 5.4 (can be changed in the `/puphpet/config.yaml` file).
* Xdebug is installed and enabled.
* MySQL 5.5.35
* The `symfony` folder is mounted in the machine to the /var/www/symfony path.
* There is one vhost [http://symfony2.dev](http://symfony2.dev/) pointing to the `/var/www/symfony/www` folder.

