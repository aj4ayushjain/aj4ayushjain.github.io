---
layout: post
title:  "Backup my work environment, setup, config etc"
date:   2021-03-06 22:22:51 +0000
categories: [opensource, setup]
---

Hey folks!
So, recently i had  switched my work setup machines and was using ssh private
public keys and some personal settings which i lost and couldn't recover them 
as well so my mentor told me to backup these settings, keys using interesting 
project.

[GHAR: home as repositories](https://github.com/philips/ghar)


So, $HOME has a bunch .file and .dir which stores application data and config 
(includes shell aliases, extension in vscode, git config file). And shifting 
to new system you need to customize, set up new ssh keys etc again which is 
much of headache.So what you can do is using ghar you could back config in git
repositories. And you just need to install and clone these repos again to bring
in your settings.

So what I will do is analyse my config files

## where/how/why should i backup them if needed

- [x] .anydesk/ - Remote machine sharing software which can be public.
- [] .bash_history - If you're pretty peculiar about what you type then surely you could it's what it's name suggests 
- [] .bash_logout - Bash related logout file for cleanup things - high level shit ;p
- [x] .bashrc or .zshrc - customize your shell,alias etc, run commands you want to run everytime you open shell
- [] .cabal/ - Haskell Package manager Recently tried to setup haskell.
- [] .cache/ - Stores the cache of all the application.
- [x] .config/ - configuration data for some apps
- [] .dropbox/ - configuration of dropbox app	
- [] .dropbox-dist/ - Directory where dropbox unpacked itself and can be exec from here
- [] .gEDA/ - Gerber file viewer
- [] .ghc/ & .ghcup/ - Glasgow Haskell Compiler related settings
- [] .gitconfig -  Configuration of global git
- [] .git-credentials - My git credentials in plaintext	
- [] .gnupg/- Program that encrypts and signs files.I don't need that i guess
- [] .ipython/ & .jupyter/ - Configuration settings for both which i don't use much.	
- [] .local/ - user specific application data for some apps
- [] .mozilla/ - I guess you shouldn't back it up as mozilla already provides sign in/sync option which is pretty great.
- [] .pki/ - Gnome-keyring related folder
- [] .profile - configuring user environments 
- [] .python_history - History of Python interpreter
- [x] .ssh/ - SSH related configs and keys
- [] .stack/ - Haskell buildup tool 
- [] .thunderbird - Email client if you have configured. I haven't
- [] .tmp/ -  Folder for temporary storage which keeps getting cleared on restart
- [x] .vscode - Vscode related configuration file 
- [] .viminfo - Store search string history,input-line history, etc stuff
- [] .wget-hsts - Database of known of GNU Wget


## You need to be carefull while backing up things

* Private git repo - .ssh, .git-credentials etc

I guess that's it for now and if you have any questions maybe we can just ping
me. [Contact](mailto:aj4ayushjain@gmail.com)
    
# REFERENCES


1. [Hidden files in my linux Home directory](https://www.maketecheasier.com/hidden-files-linux-home-directory/)

2. [local,config, cache hidden directory in $HOME ](https://askubuntu.com/questions/14535/whats-the-local-folder-for-in-my-home-directory)
