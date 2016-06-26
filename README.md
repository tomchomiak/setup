# Developer Setup


- [SSH](#SSH)
- [Hombrew](#Homebrew)
- [Atom](#Atom)
- [Node.js](#Node.js)
- [Bower](#Bower)
- [Gulp](#Gulp)
- [MongoDB](#MongoDB)
- [MongoHub](#MongoHub)
- [Redis](#Redis)


##SSH

To generate new key, paste following command in Terminal. Make sure to add a passphrase.

`ssh-keygen -t rsa -b 4096 -C "your_email@example.com"`

Add your SSH key to ssh-agent so you do not have to keep retyping your passphrase when you use your SSH key.

First check if ssh-agent is running

`eval "$(ssh-agent -s)"`

Add your SSH key to ssh-agent

`ssh-add ~/.ssh/id_rsa`


##Homebrew
Hombrew is the missing package manager for OSX.

To install, enter the following command in Terminal.

`/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`


##Atom

##Node.js

##Bower

##Gulp

##MongoDB

##MongoHub

##Redis
