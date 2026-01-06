## About pamDocs
### Useful docs for managing the pamBot docker implementation

pamBot (partnerannounce@webex.bot) is a Webex announcement bot written in python and wrapped in Flask and gunicorn.
The current Docker implementation consists of a single Docker compose stack of five containers:
* pam - the bot code running on a Ubuntu image
* pamcron - a utility image running on Ubuntu. Primarily running cron'd python scripts
* pam_mongo - pamBot's backend mongo database
* mongo-express - web-based mongo management interface
* mkdocs - server for this documentation 

Additionally, the mkdocs Docker container pulls documentation from a [github repository](https://github.com/craigjtait/pamDocs.git)
