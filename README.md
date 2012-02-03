# bm services box

A lucid32 vagrant box for developing and deploying:

 * optimorlabs.com
 * redmine

Uses the bmvagrant id, with accounts on github and gmail.

## Security Note

The vagrant box file contains an SSH key for bmvagrant@github, so the box file
needs the same security level as accounts for which bmvagrant is a collaborator,
as listed above.

## Setup

### Create .rvmrc:

    {{{
    rvm use 1.8.7
    export RUBYOPT=
    }}}

### Set up vagrant:

    gem i vagrant    # 0.9.4 or higher
    vagrant init
    vagrant box add bm-services bm-services-201201301603.box

### Save vagrant env to package.box

    vagrant package --vagrantfile Vagrantfile --include README.md

