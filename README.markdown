# sshauth

The *sshauth* puppet module provides centralized creation, distribution, and revocation of ssh keys for users.

# To install into puppet

Clone into your puppet configuration in your `puppet/modules` directory:

````
git clone git://github.com/nesi/puppet-sshauth.git sshauth
````

Or if you're managing your Puppet configuration with git, in your `puppet` directory:

````
git submodule add git://github.com/nesi/puppet-sshauth.git modules/sshauth --init --recursive
cd modules/sshauth
git checkout master
git pull
cd ../..
git commit -m "added sshauth submodule from https://github.com/nesi/puppet-sshauth"
````

It might seem bit excessive, but it will make sure the submodule isn't headless...

# Usage

To be done, but for now check http://projects.puppetlabs.com/projects/1/wiki/Module_Ssh_Auth_Patterns for usage, but replace instances of `ssh::auth`` with ``sshauth``

**Note:** if puppet is configured to use environments, key declarations *must* be in the same environment as the keymaster/puppetmaster otherwise they will not be created.

# Credits:

This module was originally created from *ssh::auth* as described in the article http://projects.puppetlabs.com/projects/1/wiki/Module_Ssh_Auth_Patterns

Which was then refactored the old auth.pp into the newer Puppet style by Atha Kouroussis: https://github.com/vurbia/puppet-sshauth

Which included these additional features
> This implementation has changed the use of virtual resources to exported resources. While it adds the burden of enabling storeconfigs, the main advantage is that keys can be declared contextually and not at central location so the keymaster can see them.

## Motives

### Forking
The *sshauth* module was forked from *sshauth* because it included work I had wanted to do (refactor into a newer puppet style) and that I wanted to include it into the Dynaguppy project (https://github.com/Aethylred/dynaguppy), which may require further modifications of the *sshauth* code, and I required a stable distribution point from which to do this.

# Gnu General Public License

This file is the sshauth Puppet module.

The sshauth Puppet module is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

The sshauth Puppet module is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with This sshauth Puppet module.  If not, see <http://www.gnu.org/licenses/>.