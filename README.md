# easyengine-backup-restore

### Install [or update / re-install] on Ubuntu 16

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
# [specify your backup settings unless previously done]
```

### Run backup script manually

```
bash nikksno/ee-br/ee-br-backup
```

### Confirm automatic daily run via cron is working

```
cat logs/ee-br-backup/latest-log
```

### Restore from backup [under development - not yet working]

```
bash nikksno/ee-br/ee-br-restore
```
