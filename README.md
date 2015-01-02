### How to backup?
Backup continuously to S3.

```
docker run -v DIRECTORY_TO_BACKUP:/backup gregory90/file-backup-s3 /app/run
```

##### Environment variables
TIMEOUT - how often perform backup, in seconds,  
DATADIR - directory from which perform backup (other than /backup),  
ACCESS_KEY - AWS S3 access key,  
SECRET_KEY - AWS S3 secret key,  
BUCKET - AWS S3 bucket for backup.  

### Restore backup
Restore file from S3.

```
docker run -v DIRECTORY_TO_RESTORE_TO:/backup gregory90/file-backup-s3 /app/restore
```

##### Environment variables
DATADIR - directory from which perform backup (other than /backup),  
ACCESS_KEY - AWS S3 access key,  
SECRET_KEY - AWS S3 secret key,  
FILE - file to restore,  
BUCKET - AWS S3 bucket for backup.
