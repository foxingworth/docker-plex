# docker-plex

It's early days. Don't use this yet.

## Mounts
* /config - Plex configuration files. They'll get generated on first run.
* /media - Mount your media files here.

## Ports
* 32400 - Needed to talk to Plex.

**TODO**: Expose more. [This article may help](https://support.plex.tv/articles/201543147-what-network-ports-do-i-need-to-allow-through-my-firewall/)

## Example usage
```
docker volume create config-plex
docker create --name plex -p 32400:32400 -v /mnt/some-usb-storage:/media -v config-plex:/config foxingworth/plex
docker start plex
```