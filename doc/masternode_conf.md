Masternode config
=======================

MNOS Core allows controlling multiple remote masternodes from a single wallet. The wallet needs to have a valid collateral output of 1500 coins for each masternode and uses a configuration file named `masternode.conf` which can be found in the following data directory (depending on your operating system):
 * Windows: %APPDATA%\MNOS\
 * Mac OS: ~/Library/Application Support/MNOS/
 * Unix/Linux: ~/.mnos/

`masternode.conf` is a space separated text file. Each line consists of an alias, IP address followed by port, masternode private key, collateral output transaction id and collateral output index.

Example:
```
mn1 127.0.0.2:16555 6w46CPH5eRdmJJgt7sM4Li9X1XREaPu8sn6tM8CugFMxLNwXkAm 4bcdf5101b7b6ee5816636b1daa18eb60e3e172f1835727ffc046a3c003c5519 0
mn2 127.0.0.4:16555 6vSdGzSqzcc6sBqoMqkwWkk2SzEC6mcXo1FMRabDyTDPyYR5oxW 4bcdf5101b7b6ee5816636b1daa18eb60e3e172f1835727ffc046a3c003c5519 1
```

In the example above:
* the collateral of 1500 MNOS for `mn1` is output `0` of transaction [4bcdf5101b7b6ee5816636b1daa18eb60e3e172f1835727ffc046a3c003c5519](https://explorer.mnos.io/tx/4bcdf5101b7b6ee5816636b1daa18eb60e3e172f1835727ffc046a3c003c5519)
* the collateral of 1500 MNOS for `mn2` is output `1` of transaction [4bcdf5101b7b6ee5816636b1daa18eb60e3e172f1835727ffc046a3c003c5519](https://explorer.mnos.io/tx/4bcdf5101b7b6ee5816636b1daa18eb60e3e172f1835727ffc046a3c003c5519)

_Note: IPs like 127.0.0.* are not allowed actually, we are using them here for explanatory purposes only. Make sure you have real reachable remote IPs in you `masternode.conf`._

The following RPC commands are available (type `help masternode` in Console for more info):
* list-conf
* start-alias \<alias\>
* start-all
* start-missing
* start-disabled
* outputs
