# easyengine-wp-backup

### Install on Ubuntu 16

```
apt update
apt -y install git
```
```
git clone https://github.com/nikksno/easyengine-autobackup
bash easyengine-autobackup/install
```
```
nano nikksno/ee-wp-bu/ee-wp-bu
# [specify your backup settings]
```

### Run manually

```
bash nikksno/ee-wp-bu/ee-wp-bu
```

### Confirm automatic daily run via cron is working

```
cat logs/ee-wp-bu/latest-log
```
