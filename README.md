# pxcli

Cli-tool to query a proxmox cluster for status of vms. Enables start/stop by passing the vmID for specific machines. Stop command uses proxmox's STOP rather than shutdown so use with care ;)

## Usage

Written in python3 and requires pythonmodule [proxmoxer](https://pypi.org/project/proxmoxer/) to connect to proxmox-api. 

```
usage: pxcli [-h] [-l] [-s vmID] [-S vmID]

CLI-tool to list status of proxmox cluster and start/stop individual VMs

optional arguments:
  -h, --help            show this help message and exit
  -l, --list-vms        Lists the status of vms
  -s vmID, --start vmID
                        Start VM with vmID
  -S vmID, --stop vmID  Stop VM with vmID
```

## Exempeloutput
```
VmHost     Status       vmID     Name
------------------------------------------------------------
vmhost9    | running    | 124   | Proxy01
vmhost9    | running    | 131   | Proxy02
vmhost8    | stopped    | 101   | DBServer01
vmhost8    | stopped    | 111   | DBServer02.migrated
vmhost9    | running    | 123   | WebServer09
``` 
