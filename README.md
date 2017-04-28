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
  --install     Install to system (/usr/bin/kodi-rpc)
  --uninstall   Uninstall from system (/usr/bin/kodi-rpc)
  -v, --version Print version and exit
  -h, --help    Show this help message and exit

Notes:
  - If connection-infos AND a config are omitted,
    "./kodi-rpc.conf" or "~/.config/kodi-rpc.conf" will be used if it exists

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
### Manual
```sh
git clone https://github.com/Tadly/kodi-rpc
./kodi-rpc/kodi-rpc --install
rm -rf ./kodi-rpc

# To uninstall it again
kodi-rpc --uninstall
```
