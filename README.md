kodi-rpc
========
Simple shell wrapper for kodis jsonrpc

## Usage
```
$ kodi-rpc --help
usage: kodi-rpc [options] [method] [params [...]]
  -H [host]     Host kodi is running on
  -P [port]     Port kodi is running on
  -u [user]     User for authentication
  -p [pass]     Password for authentication
  -c [config]   Config file to use instead of supplying
                connection infos via cli
  -h, --help    Show this help message

Notes:
  - If connection-infos AND a config are omitted,
    "/home/tadly/.config/kodi-rpc.conf" will be used if it exists

  - For playerid you may use "active" as value.
    kodi-rpc Player.PlayPause playerid active

  - Kodis jsonrpc documentation can be found here:
    http://kodi.wiki/view/JSON-RPC_API/v8

Examples:
  $ kodi-rpc Application.SetMute mute toggle
  $ kodi-rpc Application.SetVolume volume increment
  $ kodi-rpc Player.PlayPause playerid active
```

## Installation
Download [this](https://raw.githubusercontent.com/Tadly/kodi-rpc/master/kodi-rpc), put it somewhere for you to access and make sure it is executable.  
...  
...  
What??? Oh, you are lazy? Hm... I see.
```sh
curl https://raw.githubusercontent.com/Tadly/kodi-rpc/master/kodi-rpc -o kodi-rpc
chmod u+x kodi-rpc
```
