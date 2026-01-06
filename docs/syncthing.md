# Syncthing
### Used to synchronize Docker and Mongo data between pamBot hosts
[Link to Syncthing](https://syncthing.net/)

### Setting up Syncthing auto start (systemctl)
[Auto start documentation](https://docs.syncthing.net/users/autostart.html#checking-the-service-status)

* [Download service file](https://github.com/syncthing/syncthing/raw/main/etc/linux-systemd/system/)

* sudo cp /Downloads/syncthing@.service /etc/systemd/system

* systemctl enable syncthing@ctait.service

* systemctl start syncthing@ctait.service

* systemctl status syncthing@myuser.service

