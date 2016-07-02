# Developer Setup

Recommended setup for Node.js Developer on Mac

- [Git](#git)
- [SSH](#ssh)
- [Hombrew](#homebrew)
- [Atom](#atom)
- [Node.js](#nodejs)
- [PM2](#pm2)
- [Bower](#bower)
- [Gulp](#gulp)
- [MongoDB](#mongodb)
- [MongoHub](#mongoHub)
- [Redis](#redis)
- [Postman](#postman)
- [VirtualBox](#virtualbox)



##Git

Configure git

``` bash
git config --global user.name "Your Name Here"
git config --global user.email "your_email@youremail.com"
```

Verify Github.com SSH key fingerprints when pushing to Github for first time

These are GitHub's public key fingerprints (in hexadecimal format):

```bash
16:27:ac:a5:76:28:2d:36:63:1b:56:4d:eb:df:a6:48 (RSA)
ad:1c:08:a4:40:e3:6f:9c:f5:66:26:5d:4b:33:5d:8c (DSA)
```

These are the SHA256 hashes shown in OpenSSH 6.8 and newer (in base64 format):

```bash
SHA256:nThbg6kXUpJWGl7E1IGOCspRomTxdCARLviKw6E5SY8 (RSA)
SHA256:br9IjFspm1vxR3iA35FWE+4VTyz1hYVLIE2t1/CeyWQ (DSA)
```

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

Get Atom editor [here](https://atom.io/)

##Node.js

Install Node.js using NVM.

```bash
brew update
brew install nvm
mkdir ~/.nvm
nano ~/.bash_profile
```

In your .bash_profile file, add the following:

```bash
export NVM_DIR=~/.nvm
source $(brew --prefix nvm)/nvm.sh
```

activate nvm

```bash
source ~/.bash_profile
echo $NVM_DIR
```

To download, compile, and install the latest v6.x.x release of node, do this:

```bash
nvm install 6
```
to show current node version

```bash
node --version
```

You will have to `npm install -g` your global dependencies for each version.

Switch of node version like so

```bash
nvm use 0.10
```

To show node versions currently installed with nvm

```bash
nvm ls
```

##PM2
To install pm2

```bash
npm install pm2 -g
```

##Bower

Install bower globally

```bash
npm install -g bower

```

To install packages and save to bower.json

```bash
bower install <package> --save
```
To uninstall unused packages

```bash
bower prune
```

To update bower package

```bash
bower update <name> [<name> ..] [<options>]
```

update options

* -F, --force-latest: Force latest version on conflict
* -S, --save: Update dependencies in bower.json
* -D, --save-dev: Update devDependencies in bower.json


##Gulp

Gulp is a popular, streaming build system. You will want to install Gulp globally

```bash
npm install --global gulp-cli
```

If you have an old version of Gulp already installed then you will need to uninstall it before continuing `npm rm --global gulp`

When using Gulp in your projects, make sure to all install Gulp as a dev-dependency

```bash
npm init
npm install --save-dev gulp
```


##MongoDB

Use homebrew to install MongoDB.

```bash
brew update
brew install mongodb
```

This will install MongoDB in `/usr/local/Cellar/mongodb/`

MongoDB configuration file should be located here `/usr/local/etc/mongod.conf`

MongoDB logs will be here `/usr/local/var/log/mongodb/mongo.log`

And default db path will be here `/usr/local/var/mongodb`

You can run MongoDB process manually like so.

```bash
mongod --config /usr/local/etc/mongod.conf
```
Its best to have the MongoDB process run in the background and persist reboots.

```bash
//Start mongod process on session start after reboot
ln -sfv /usr/local/opt/mongodb/*.plist ~/Library/LaunchAgents

//Start MongoDB in background and keep it running
launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist
```


##MongoHub

##Redis

##Postman

Get postman [here](https://www.getpostman.com/)
