# Robot Framework in Vagrant

## Requirements

 * [VirtualBox](https://www.virtualbox.org)
 * [Vagrant](https://www.vagrantup.com)
 * An X Windows Server, pick one:
  * Mac OS: [XQuartz](http://xquartz.macosforge.org/)
  * Windows: [Xming](http://www.straightrunning.com/XmingNotes/) (Donationware)
  * Windows: [VcXsrv](https://sourceforge.net/projects/vcxsrv/?source=typ_redirect) (Freeware)
  * Linux: Built into "workstation" distro builds

## Usage

``` console
$ cd vagrant-robot-framework

$ vagrant up
# Download/configure/starts the VM.  First time takes 8-9 minutes on broadband.

$ vagrant ssh
# Log into the VM, to do commands manually, OR:

$ vagrant ssh -c 'pybot src/path/to/your/test'
# Run test(s) in that directory, and all subdirectories, OR:

$ vagrant ssh -c 'pybot src/path/to/your/test' -- -x
# Run test(s)s in headless mode, OR
```

## What's Inside?

 * Python 2.7
 * pip
 * VirtualEnv
 * Robot Framework 2.8.6
 * Selenium2Library 1.6.0
 * Firefox
 * Xvfb
