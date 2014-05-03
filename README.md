VAGRANT-DEVSTACK (Another vagrant devstack box)
================================================

This box can be used to test devstack on a Vagrant box.

Usage
-----

```
$ vagrant up
```

You can then access to Horizon (devstack dashboard) at : http://192.168.33.11 (login : admin / passwd : admin) and try to create new VM.

Default security group has been updated in order to allow ICMP and SSH (see vagrant provisionning).

Tips 
----

If you want to allow guests in DevStack to talk to outside world

```
sudo iptables -t nat -A POSTROUTING -o eth0 -j MASQUERADE
```

source : https://ask.openstack.org/en/question/1830/allowing-guests-in-devstack-to-talk-to-outside-world/

Ressources
-----------

* Install devstack on a single-machine : http://devstack.org/guides/single-machine.html
