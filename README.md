RabbitMQ VM
===========

Contains a RabbitMQ VM, and pre-installed php-amqplib.

To setup
--------

```
$ git clone git@github.com:asgrim/rmq-vm.git
```

Or if you have the repository on a USB drive, simply copy onto your local machine in your preferred folder.

If copied from USB drive
------------------------

If you copied the repository from the USB drive, you will already have the `rmq-vm.box`. Simply:

```
$ cd /path/to/rmq-vm/
$ vagrant box add asgrim/rmq-vm rmq-vm.box
$ vagrant up --no-provision
```

Without a pre-existing .box file
--------------------------------

**WARNING: This will take a long time on slow connections. Do not use at a conference, unless you like waiting a lot.**

```
$ vagrant up
```
