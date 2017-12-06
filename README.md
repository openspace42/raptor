# EasyEngine-Backup-Restore

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
