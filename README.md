symfony2-project-vagrant
========================

Symfony 2 Vagrant is a tool for building and distributing development environments.

Vagrant provides the framework and configuration format to create and
manage complete portable development environments. These development
environments can live on your computer or in the cloud, and are portable
between Windows, Mac OS X, and Linux.

Vagrant Install
---------------

```
vagrant init hashicorp/precise64
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

