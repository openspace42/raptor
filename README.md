# EasyEngine-Backup-Restore

### Features

* **One touch, three minute install**
* **Set it and forget it**, will automatically run a backup every night and email you in case of failure
* Works with **all easyengine site types**
* **Perfectly restores every aspect of every single easyengine website you're hosting**, from your database, to your files, and so on
* Stores backups both **locally and remotely [on S3]**
* **Encrypts** all remote backups with a 42 character passphrase
* Allows you to restore your backup with **one single command** and a maximum of **three minutes of your time** even from a blank machine you've never set up before
* Performs DNS checks and **prompts you to activate LetsEncrypt** on newly restored sites [work in progress...]
* Does NOT rely on easyengine's database but rather **directly scans your /var/www/ directory**
* Performs a test restore before every backup to **ensure remote backup integrity and passphrase match**
* Returns **detailed errors in case of failure** to help you get your data back during a restore


### Install [or update / re-install] on Ubuntu 16

```
apt update
apt -y install git
```
```
git clone https://github.com/openspace42/EasyEngine-Backup-Restore
bash EasyEngine-Backup-Restore/install
```
```
nano openspace42/ee-br/config
# [specify your backup settings unless previously done]
```

### Run backup script manually

```
bash openspace42/ee-br/ee-br-backup
```

### Confirm automatic daily run via cron is working

```
cat logs/ee-br-backup/latest-log
```

### Restore from backup [under development - not yet working]

```
bash openspace42/ee-br/ee-br-restore
```
