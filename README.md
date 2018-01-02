# EasyEngine-Backup-Restore

## Video overview [11 minutes]

[![EasyEngine-Backup-Restore youtube video](https://img.youtube.com/vi/sw3FsBWHj9M/maxresdefault.jpg)](https://www.youtube.com/watch?v=sw3FsBWHj9M)

<a href="http://www.youtube.com/watch?feature=player_embedded&v=sw3FsBWHj9M" target="_blank"><img src="http://img.youtube.com/vi/sw3FsBWHj9M/maxresdefault.jpg" alt="EasyEngine-Backup-Restore youtube video" width="457" height="257" border="10" /></a>

## Features

* **One touch, three minute install**
* **Set it and forget it**, will automatically run a backup every night and email you in case of failure
* Works with **all easyengine site types**
* **Perfectly restores every aspect of every single easyengine website you're hosting**, from your database, to all of your files [even outside htdocs], and so on
* Stores backups both **locally and remotely [on S3]**
* **Encrypts** all remote backups with a 42 character passphrase
* Allows you to restore your backup with **one single command** and a maximum of **three minutes of your time** even from a blank machine you've never set up before
* Performs DNS checks and **prompts you to activate LetsEncrypt** on newly restored sites
* Does NOT rely on easyengine's database but rather **directly scans your /var/www/ directory**
* Performs a test restore before every backup to **ensure remote backup integrity and passphrase match**
* Actually [re-]installs and updates EasyEngine on install and restore operations to remove any extra step: you'll be fully operational with just one command
* Returns **detailed errors in case of failure** to help you get your data back during a restore


## Install [or update / re-install] [tested on Debian 8 and Ubuntu 16]

Current version: v0.0.1 [2018-01-01]

```
apt update
apt -y install git
```
```
git clone https://github.com/openspace42/EasyEngine-Backup-Restore
bash EasyEngine-Backup-Restore/setup
```
```
nano openspace42/ee-br/config
# [specify your backup settings unless previously done]
```

## Backing up

### Run backup script manually

```
bash openspace42/ee-br/ee-br-backup
```

### Confirm automatic daily run via cron is working

```
cat logs/ee-br-backup/latest-log
```

## Restoring

### Preparation [only if this is a new machine]

1. Run the installer as detailed above in the "Install" section
2. Edit the `openspace42/ee-br/config` file to ensure your backup/restore method is correct [local / s3] and if necessary specify your backup passphrase.

### Actually restoring

```
bash openspace42/ee-br/ee-br-restore
```

### Advanced usage

See the [Advanced Restore](https://github.com/openspace42/EasyEngine-Backup-Restore/wiki/Advanced-Restore) wiki page for runtime arguments.
