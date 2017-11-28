# easyengine-backup-restore

### Install on Ubuntu 16

```
apt update
apt -y install git
```
```
git clone https://github.com/nikksno/easyengine-backup-restore
bash easyengine-backup-restore/install
```
```
nano nikksno/ee-br/config
# [specify your backup settings]
```

### Run backup script manually

```
bash nikksno/ee-br/ee-br-backup
```

### Confirm automatic daily run via cron is working

```
cat logs/ee-br-backup/latest-log
```
