# Dockstar: Darkstar Made Easy
Dockstar lets you configure, build, and deploy a new Darkstar server with zero effort.

# Quick-Start
0. Ensure your system supports the BASH shell (Mac OS and Linux automatically have this)
1. Run `git clone https://github.com/crahda/dockstar` in a terminal
2. `cd dockstar`
3. `bash build.sh` (wait a very long time)
4. `bash start.sh` (wait a moderate amount of time the first time)
5. A Darkstar server will now be running at your computer's public IP address. Enjoy!

# Configuration
All of the configuration options can be found in the `conf` folder. ***DO NOT*** change any of the values labeled as `DS_USERNAME`, `DS_PASSWORD`, or `DS_SERVERNAME`; these values are automatically replaced whenever the server is rebuilt. When you are satified with your configuration changes, you must re-run `bash build.sh` for the changes to take effect.

## Game Masters
Whenever the Dockstar server is started via `bash start.sh`, it will look for an array environment variable called `DS_GMS_LIST`. If this variable exists and contains the names of any characters in the game world, those characters will be automatically promoted to level 5 GMS. Here's an example configuration you could perform to make `Crahda` and `Rickie` GMs:

    export DS_GMS_LIST=("Crahda" "Rickie")

## Zone IP
Whenever the Dockstar server is started via `bash start.sh`, it will automatically configure the Zone IP to be your computers public IP address. To override this with a custom domain or other thing, simply run the following command at your command line, replacing `my.domain.com` with your desired public IP:

    export ZONE_IP=my.domain.com

# Updating
1. `git pull`
2. `bash build.sh`