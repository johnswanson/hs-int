# Vagrant VM for the Hardware Software Interface Course #

## Purpose ##
I generally hate working in VMs because it requires me to reconfigure my development environment. And it's never quite as comfortable working in a VM.

Vagrant comes in handy here. It's essentially a wrapper for VirtualBox that makes it really easy to create headless VMs and configure them.

You should probably only install this if you're comfortable with the command line, as if you want a GUI you're better off using something like VirtualBox.

## Instructions ##
If anything, this should be *easier* than the standard installation method. (Just note that I can't guarantee that this configuration is perfect.)

1. [Install Vagrant](http://docs.vagrantup.com/v2/installation/).
2. [Download](http://example.com/hs-int.box) (broken link, will be replaced shortly) the Vagrant box I've created--essentially the instructor-provided VM in a different package, although I had to make a few changes to get it working with Vagrant.
3. Clone this repository, then go to it and run "vagrant up"

		git clone git@github.com:johnswanson/hs-int
		cd hs-int
		vagrant up

4. You're now running Fedora! It's "headless", though, which means there's no GUI.

		vagrant ssh
		
	is a quick way to ssh into the VM. You'll need to do this to run the instructor-provided setup scripts (to change passwords) and compile and run your programs! *NOTE:* the password for *auser* is "password".
	
	What's so great about all this? Well, the "auser" folder in this repo is synced with the /home/auser folder on the VM. So you can edit all the files for this course on your host computer, but compile and run them on the guest Fedora OS.
5. When you're done, run

		vagrant destroy

## Contact ##
John Swanson

johndswanson@gmail.com
