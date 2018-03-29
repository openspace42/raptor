# raptor

## Features

* **One touch, three minute install**
* **Fully installs EasyEngine** with all extra modules from the start and more
* **Set-it-and-forget-it backups** will automatically run a backup of all your sites every night and email you in case of failure
* Works with **all EasyEngine site types**
* Stores backups both **locally and remotely [on S3]**
* **Encrypts** all remote backups with a 42 character passphrase
* **Backs up new sites automatically** with no need to perform any additional action
* **Requires no operations inside the individual websites**, everything happens on the filesystem level completely unbeknownst to the websites themselves
* Does NOT rely on EasyEngine's database but rather **directly scans your /var/www/ directory**
* Performs a **test restore** before every S3 backup to **ensure remote backup integrity and passphrase match**
* Allows you to restore your backup with **one single command** and a maximum of **three minutes of your time** even from a blank machine you've never set up before
* **Perfectly restores every aspect of every single EasyEngine website you're hosting**, from your database, to all of your files [even outside htdocs], and so on
* Performs DNS checks and **prompts you to activate LetsEncrypt** on newly restored sites
* Actually [re-]installs and updates EasyEngine on install and restore operations to remove any extra step: you'll be fully operational with just one command
* Returns **detailed errors in case of failure** to help you get your data back during a restore
* Outputs clean and colorful logs and stores them automatically inside its own log directory


## Install [or update / re-install] [tested on Debian 8 and Ubuntu 16]

```
[log in as root on your EasyEngine linux server]
cd
```

```
apt update
apt -y install git
```
```
git clone https://github.com/openspace42/raptor
bash raptor/setup
```


## Backing up

### Run backup script manually

```
bash openspace42/raptor/tools/raptor-backup
```

### Confirm automatic daily run via cron is working

```
cat logs/raptor-backup/latest-log
```

## Restoring

### Preparation [only if this is a new machine]

1. Run the installer as detailed above in the "Install" section

### Actually restoring

```
bash openspace42/raptor/tools/raptor-restore
```

### Advanced usage

See the [Advanced Restore](https://github.com/openspace42/raptor/wiki/Advanced-Restore) wiki page for runtime arguments.
