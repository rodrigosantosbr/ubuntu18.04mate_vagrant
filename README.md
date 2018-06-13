# ubuntu18.04mate_vagrant
Vagrant File for Ubuntu 18.04

## Last update/tests

```
2018-06-13
```

### Prerequisites

```
Internet connection
Oracle Virtualbox >= 5.2.12 installed
Vagrant installed
Babun Shell installed (if Windows) - http://babun.github.io/
```

### Login and password

```
login: vagrant
password: vagrant
```

## Running

On Vagrantfile dir:

```
vagrant up 
vagrant provision
```

## Useful commands

To reload a VM and reload any new changes in the Vagrantfile config run

```
vagrant reload
```

When complete and want to exit, run

```
vagrant halt
```

When you are ready to start working again and starting fresh

```
vagrant up
```

## SSH

Add host user's ssh public key to authorized_host
private_key file (On Windows) - C:/<<my_vagrantfile_dir>>/.vagrant/machines/default/virtualbox/private_key

```
ssh-keygen -y -f C:/vagrant/.vagrant/machines/default/virtualbox/private_key | ssh -p 2222 -o UserKnownHostsFile=/dev/null vagrant@127.0.0.1 "cat >> ~/.ssh/authorized_keys
```

Establishing ssh connection

```
ssh -p 2222 -o UserKnownHostsFile=/dev/null -i C:/vagrant/.vagrant/machines/default/virtualbox/private_key vagrant@127.0.0.1
```

Tip: change authorized_keys on VM

```
chmod 644 /home/vagrant/.ssh/authorized_keys
```
