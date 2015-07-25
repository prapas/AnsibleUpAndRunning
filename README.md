# AnsibleUpAndRunning

setup your MBP
- install Homebrew (http://brew.sh/)
- -- ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

==> This script will install:
/usr/local/bin/brew
/usr/local/Library/...
/usr/local/share/man/man1/brew.1

Press RETURN to continue or any other key to abort
==> /usr/bin/sudo /bin/mkdir /Library/Caches/Homebrew
Password:
==> /usr/bin/sudo /bin/chmod g+rwx /Library/Caches/Homebrew
==> Downloading and installing Homebrew...
remote: Counting objects: 3668, done.
remote: Compressing objects: 100% (3500/3500), done.
remote: Total 3668 (delta 38), reused 648 (delta 28), pack-reused 0
Receiving objects: 100% (3668/3668), 2.99 MiB | 1.23 MiB/s, done.
Resolving deltas: 100% (38/38), done.
From https://github.com/Homebrew/homebrew
 * [new branch]      master     -> origin/master
HEAD is now at 71f6a4c libgcrypt: use https for resource
==> Installation successful!
==> Next steps
Run `brew help` to get started

- install VirtualBox
-- https://www.virtualbox.org/wiki/Downloads
- install Vagrant
-- http://www.vagrantup.com/downloads


setup Ansible control machine
- install Python 2.6 or later
-- brew install python

==> Installing dependencies for python: readline, sqlite, gdbm, openssl
==> Installing python dependency: readline
==> Downloading https://homebrew.bintray.com/bottles/readline-6.3.8.yosemite.bottle.tar.gz
######################################################################## 100.0%
==> Pouring readline-6.3.8.yosemite.bottle.tar.gz
==> Caveats
This formula is keg-only, which means it was not symlinked into /usr/local.

OS X provides similar software, and installing this software in
parallel can cause all kinds of trouble.

OS X provides the BSD libedit library, which shadows libreadline.
In order to prevent conflicts when programs look for libreadline we are
defaulting this GNU Readline installation to keg-only.

Generally there are no consequences of this for you. If you build your
own software and it requires this formula, you'll need to add to your
build variables:

    LDFLAGS:  -L/usr/local/opt/readline/lib
    CPPFLAGS: -I/usr/local/opt/readline/include

==> Summary
🍺  /usr/local/Cellar/readline/6.3.8: 40 files, 2.1M
==> Installing python dependency: sqlite
==> Downloading https://homebrew.bintray.com/bottles/sqlite-3.8.10.2.yosemite.bottle.tar.gz
######################################################################## 100.0%
==> Pouring sqlite-3.8.10.2.yosemite.bottle.tar.gz
==> Caveats
This formula is keg-only, which means it was not symlinked into /usr/local.

OS X already provides this software and installing another version in
parallel can cause all kinds of trouble.

OS X provides an older sqlite3.

Generally there are no consequences of this for you. If you build your
own software and it requires this formula, you'll need to add to your
build variables:

    LDFLAGS:  -L/usr/local/opt/sqlite/lib
    CPPFLAGS: -I/usr/local/opt/sqlite/include

==> Summary
🍺  /usr/local/Cellar/sqlite/3.8.10.2: 9 files, 2.8M
==> Installing python dependency: gdbm
==> Downloading https://homebrew.bintray.com/bottles/gdbm-1.11.yosemite.bottle.2.tar.gz
######################################################################## 100.0%
==> Pouring gdbm-1.11.yosemite.bottle.2.tar.gz
🍺  /usr/local/Cellar/gdbm/1.11: 17 files, 532K
==> Installing python dependency: openssl
==> Downloading https://homebrew.bintray.com/bottles/openssl-1.0.2d_1.yosemite.bottle.tar.gz
######################################################################## 100.0%
==> Pouring openssl-1.0.2d_1.yosemite.bottle.tar.gz
==> Caveats
A CA file has been bootstrapped using certificates from the system
keychain. To add additional certificates, place .pem files in
  /usr/local/etc/openssl/certs

and run
  /usr/local/opt/openssl/bin/c_rehash

This formula is keg-only, which means it was not symlinked into /usr/local.

OS X already provides this software and installing another version in
parallel can cause all kinds of trouble.

Apple has deprecated use of OpenSSL in favor of its own TLS and crypto libraries

Generally there are no consequences of this for you. If you build your
own software and it requires this formula, you'll need to add to your
build variables:

    LDFLAGS:  -L/usr/local/opt/openssl/lib
    CPPFLAGS: -I/usr/local/opt/openssl/include

==> Summary
🍺  /usr/local/Cellar/openssl/1.0.2d_1: 464 files, 18M
==> Installing python
==> Downloading https://homebrew.bintray.com/bottles/python-2.7.10_2.yosemite.bottle.tar.gz
######################################################################## 100.0%
==> Pouring python-2.7.10_2.yosemite.bottle.tar.gz
==> Caveats
Pip and setuptools have been installed. To update them
  pip install --upgrade pip setuptools

You can install Python packages with
  pip install <package>

They will install into the site-package directory
  /usr/local/lib/python2.7/site-packages

See: https://github.com/Homebrew/homebrew/blob/master/share/doc/homebrew/Homebrew-and-Python.md


.app bundles were installed.
Run `brew linkapps python` to symlink these to /Applications.
==> /usr/local/Cellar/python/2.7.10_2/bin/python -s setup.py --no-user-cfg install --force --verbose --single-version-externally-managed --record=installed.txt --install-scripts=/usr/local/Cellar/python/2.7.10_2/bin --install-li
==> /usr/local/Cellar/python/2.7.10_2/bin/python -s setup.py --no-user-cfg install --force --verbose --single-version-externally-managed --record=installed.txt --install-scripts=/usr/local/Cellar/python/2.7.10_2/bin --install-li
==> /usr/local/Cellar/python/2.7.10_2/bin/python -s setup.py --no-user-cfg install --force --verbose --single-version-externally-managed --record=installed.txt --install-scripts=/usr/local/Cellar/python/2.7.10_2/bin --install-li
==> Summary
🍺  /usr/local/Cellar/python/2.7.10_2: 4866 files, 76M

python --version
Python 2.7.10


- install Ansible
-- brew install ansible
==> Installing ansible dependency: libyaml
==> Downloading https://homebrew.bintray.com/bottles/libyaml-0.1.6_1.yosemite.bottle.tar.gz
######################################################################## 100.0%
==> Pouring libyaml-0.1.6_1.yosemite.bottle.tar.gz
🍺  /usr/local/Cellar/libyaml/0.1.6_1: 7 files, 352K
==> Installing ansible
==> Downloading https://homebrew.bintray.com/bottles/ansible-1.9.2.yosemite.bottle.tar.gz
######################################################################## 100.0%
==> Pouring ansible-1.9.2.yosemite.bottle.tar.gz
🍺  /usr/local/Cellar/ansible/1.9.2: 3594 files, 42M

- create vm from vagrant
-- mkdir ~/Downloads/AnsibleUpAndRunning
-- cd ~/Downloads/AnsibleUpAndRunning
-- mkdir playbooks
-- cd playbooks/
-- vagrant init ubuntu/trusty64
A `Vagrantfile` has been placed in this directory. You are now
ready to `vagrant up` your first virtual environment! Please read
the comments in the Vagrantfile as well as documentation on
`vagrantup.com` for more information on using Vagrant.
-- vabrant up
Bringing machine 'default' up with 'virtualbox' provider...
==> default: Box 'ubuntu/trusty64' could not be found. Attempting to find and install...
    default: Box Provider: virtualbox
    default: Box Version: >= 0
==> default: Loading metadata for box 'ubuntu/trusty64'
    default: URL: https://atlas.hashicorp.com/ubuntu/trusty64
==> default: Adding box 'ubuntu/trusty64' (v20150609.0.10) for provider: virtualbox
    default: Downloading: https://atlas.hashicorp.com/ubuntu/boxes/trusty64/versions/20150609.0.10/providers/virtualbox.box
    default: Progress: 6% (Rate: 969k/s, Estimated time remaining: 0:08:06)
==> default: Successfully added box 'ubuntu/trusty64' (v20150609.0.10) for 'virtualbox'!
==> default: Importing base box 'ubuntu/trusty64'...
==> default: Matching MAC address for NAT networking...
==> default: Checking if box 'ubuntu/trusty64' is up to date...
==> default: Setting the name of the VM: playbooks_default_1437807266545_23366
==> default: Clearing any previously set forwarded ports...
==> default: Clearing any previously set network interfaces...
==> default: Preparing network interfaces based on configuration...
    default: Adapter 1: nat
==> default: Forwarding ports...
    default: 22 => 2222 (adapter 1)
==> default: Booting VM...
==> default: Waiting for machine to boot. This may take a few minutes...
    default: SSH address: 127.0.0.1:2222
    default: SSH username: vagrant
    default: SSH auth method: private key
    default: Warning: Connection timeout. Retrying...
    default: 
    default: Vagrant insecure key detected. Vagrant will automatically replace
    default: this with a newly generated keypair for better security.
    default: 
    default: Inserting generated public key within guest...
    default: Removing insecure key from the guest if it's present...
    default: Key inserted! Disconnecting and reconnecting using new SSH key...
==> default: Machine booted and ready!
==> default: Checking for guest additions in VM...
==> default: Mounting shared folders...
    default: /vagrant => /Users/xxxxx/Downloads/AnsibleUpAndRunning/playbooks
  
-- vagrant ssh
Welcome to Ubuntu 14.04.2 LTS (GNU/Linux 3.13.0-55-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sat Jul 25 06:54:45 UTC 2015

  System load:  0.27              Processes:           84
  Usage of /:   3.2% of 39.34GB   Users logged in:     0
  Memory usage: 26%               IP address for eth0: 10.0.2.15
  Swap usage:   0%

  => There are 3 zombie processes.

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.

-- vagrant ssh-config
Host default
  HostName 127.0.0.1
  User vagrant
  Port 2222
  UserKnownHostsFile /dev/null
  StrictHostKeyChecking no
  PasswordAuthentication no
  IdentityFile /Users/xxxxx/Downloads/AnsibleUpAndRunning/playbooks/.vagrant/machines/default/virtualbox/private_key
  IdentitiesOnly yes
  LogLevel FATAL


-- ssh vagrant@127.0.0.1 -p 2222 -i  /Users/xxxxx/Downloads/AnsibleUpAndRunning/playbooks/.vagrant/machines/default/virtualbox/private_key
The authenticity of host '[127.0.0.1]:2222 ([127.0.0.1]:2222)' can't be established.
RSA key fingerprint is fc:fa:3e:ec:3e:7c:00:2e:a4:9b:9d:34:31:8e:fa:b8.
Are you sure you want to continue connecting (yes/no)? yes
Warning: Permanently added '[127.0.0.1]:2222' (RSA) to the list of known hosts.
Welcome to Ubuntu 14.04.2 LTS (GNU/Linux 3.13.0-55-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sat Jul 25 06:58:01 UTC 2015

  System load:  0.01              Processes:           75
  Usage of /:   3.2% of 39.34GB   Users logged in:     0
  Memory usage: 24%               IP address for eth0: 10.0.2.15
  Swap usage:   0%

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.


Last login: Sat Jul 25 06:58:01 2015 from 10.0.2.2
vagrant@vagrant-ubuntu-trusty-64:~$ 

