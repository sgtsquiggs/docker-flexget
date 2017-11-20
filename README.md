[![](https://images.microbadger.com/badges/image/sgtsquiggs/flexget.svg)](https://microbadger.com/images/sgtsquiggs/flexget)

# flexget

[FlexGet](https://github.com/Flexget/Flexget) is a multipurpose automation tool for content
like torrents, nzbs, podcasts, comics, series, movies, etc.

## Usage
```
docker run \
    --name=flexget \
    -v <path to data>:/config \
    -e PGID=<gid> -e PUID=<uid> \
    sgtsquiggs/flexget
```

## Parameters
* `-v <path>:/config` where configuation files are stored.
* `-e PGID=<gid>` for Group ID (see below)
* `-e PUID=<uid>` for User ID (see below)

## User and Group ID
Set these to match the user/group ID of shared data volumes. Files written to these volumes
will match the provided uid/gid.

## Acknowledgements

* [lsiobase/alpine](https://github.com/linuxserver/docker-baseimage-alpine)
