# Mongo miscellaneous:
## On pam_mongo container: <-- at some point, cron mongodump and change syncthing 
The mongo container mounts a local bind mount volume (/data/remote_data) containing a mongo dump of the 
partnerbot database. This dump is sync'd bewteen the two Docker hosts using syncthing. Currently, the 
dump isn't scheduled to occur automatically, but I'll work on getting that automated.

### Dump / backup the database
* mongodump --db partnerbot --out /data/remote_data
### Restore the database
* mongorestore --db partnerbot /data/remote_data/partnerbot
