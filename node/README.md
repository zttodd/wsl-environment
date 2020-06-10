# node / npm  

## Installation  

This guide will install Node and npm using a Node version manager called `n`:

https://github.com/tj/n  

The default way to install `n` is through `npm`, but we can bootstrap `n` so that we won't need an extra installation of Node on our machine.  

First, let's `cd` into our home directory and get a copy of `n`:  

`curl -L https://raw.githubusercontent.com/tj/n/master/bin/n -o n`  

Next, let's temporarily set a location for `n` to install Node/npm (this won't persist to a new terminal instance, so this line will also need to be added to your `.bashrc` or `.zshrc` file):  

`export N_PREFIX=$HOME/.n`  

Finally, let's install the `lts` version of Node into the location set in the previous step:  

`bash n lts`  

### Set the PATH  

Add the following line to your shell's configuration file to update the PATH to find the Node installations. This will need to be set _after_ the `N_PREFIX` export:  

`export PATH=$N_PREFIX/bin:$PATH`  

### Checking the installation  

Try out your new Node/npm installation by checking the versions on each:  

`node -v`  
`npm -v`  
