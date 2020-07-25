# Ruby  

## Prerequisites  

Before we get started, make sure the following packages are installed in Ubuntu:  

`sudo apt install build-essential libreadline-dev libssl-dev zlib1g-dev`

## rbenv

### Download and install rbenv

This guide will set up an environment to install Ruby using a version manager called `rbenv`:  
https://github.com/rbenv/rbenv  

The following steps are pulled from the `rbenv` GitHub repo's README. Since we're using Linux, we'll follow the manual instructions instead of the Homebrew (MacOS) steps.

First, let's `cd` into our home directory and clone a copy of `rbenv` into `~/.rbenv`:  
`git clone https://github.com/rbenv/rbenv.git ~/.rbenv`  

### Set the PATHs

Next, let's add `rbenv` to our PATH by adding the following line to the `.bashrc` (or `.zshrc`) file:  
`export PATH="$HOME/.rbenv/bin:$PATH"`  

Set up `rbenv` in the shell:  
`~/.rbenv/bin/rbenv init`  

Restart your terminal or source your shell's rc file for the PATH changes to take effect.

### Installing ruby-build  

Install the `ruby-build` plugin with the following command:  
`git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build`  

### Verify the rbenv setup

Use the `rbenv-doctor` script to verify that `rbenv` was set up correctly:  
`curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash`

## Install ruby  

Using `rbenv`, let's install a version of Ruby. Use the following command to list all available versions:  
`rbenv install -l`  

At the time of these docs, version `2.7.1` is the latest, so let's install that one:  
`rbenv install 2.7.1`  

Once Ruby has installed, you can set it as your global, default version to use with the following:  
`rbenv global 2.7.1`  

After restarting your terminal, Ruby should now be available for use!