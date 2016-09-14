# RabbitMQ VM

Last packaged: 14th September 2016 (includes RabbitMQ 3.6.5).

## Usage instructions

Contains a RabbitMQ VM, and pre-installed php-amqplib.

### To setup

```
$ git clone git@github.com:asgrim/rmq-vm.git
```

Or if you have the repository on a USB drive, simply copy onto your local machine in your preferred folder.

### If copied from USB drive

If you copied the repository from the USB drive, you will already have the `rmq-vm.box`. Simply:

```
$ cd /path/to/rmq-vm/
$ vagrant box add asgrim/rmq-vm rmq-vm.box
$ vagrant up --no-provision
```

### Without a pre-existing .box file

**WARNING: This will take a long time on slow connections. Do not use at a conference, unless you like waiting a lot.**

```
$ vagrant up
```

## Repackagaing

 * Perform updates as necessary, latest RabbitMQ, ensure plugins work (especially community plugin `rabbitmq_delayed_message_exchange`)
 * Run `vagrant package --output rmq-vm-{Y-m-d}.box`
 * Upload to Dropbox
 * Add link to `Vagrantfile`
 * Update the `README.md` with latest packaging.
 * Copy the box to USB (call it `rmq-vm.box` so instructions match)

## Troubleshooting

OSX users may encounter issues bringing the box up (solution thanks to @svpernova09, see [tweet](https://twitter.com/JoePFerguson/status/735108862043267072))!

You'll most likely need to edit the `.vagrant/machines/default/virtualbox/creator_uid` file and change 1000 to 501 (or whatever your user's ID is on your system).
