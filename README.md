# regular Redis backup

## clone the repository to /opt/redis-backup with the following command
```sudo mkdir -p /opt/redis-backup && sudo chown $USER:root /opt/redis-backup && git clone git@github.com:szilveszter9/redis-backup.git /opt/redis-backup```
## example: install cron job for daily backup to your /mnt/ramdisk/ where you want to keep your backups for 7 days and your redis password is SeCrEtPw
```/opt/redis-backup/install.sh \* \* \* \* \* /mnt/ramdisk/ 7 SeCrEtPw```
## this will install two cron jobs, one for the backup one for the cleanup, check with
```crontab -l```