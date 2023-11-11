
# media_stacks

## General
`/config` is a folder that holds configuration for these containers.  I opted for `/config/{appname}` as a pattern

I also opted to give each app access to the root of each drive.

## Server Config
- Make the `/config` folder
- Add the drives to fstab
    - `sudo blkid`  to get the `LABEL` or `UUID` info about each drive
    - `sudo nano /etc/fstab` to add the volumes:

    ````
    LABEL=volume4   /volume4        ntfs    defaults        0       0
    LABEL=volume5   /volume5        ntfs    defaults        0       0    
    ````

    Can be either tabs or spaces.  `ntfs` is the format, no idea about `defaults` or the `0`s

## Applications

### Heimdall 
Dashboard to link to everything

### Flaresolverr
Wires into other containers as a way of solving captchas.

### Prowlarr
Centralized search

### Transmission Open VPN
Transmission web client with VPN.

### sabnzbd
Usenet downloader

### Sonarr
TV shows

### Radarr
Movies

### Readarr
Books

### Jellyfin
Media center 

### Docker compose that I keep forgetting
`docker compose -f file name.yml up -d`
`docker compose -f file name.yml down`