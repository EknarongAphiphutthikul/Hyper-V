# Hyper-V
## Create Virtual Switch Type Internal
For internal cluster
```powershell
New-VMSwitch -SwitchName "vEthernet-Internal-ME" -SwitchType Internal
```
<br/>

## Create Virtual Switch Type External
For VM connect to internet
- Show adapter
```powershell
Get-NetAdapter
```
- create virtual switch external
```powershell
  New-VMSwitch -name "vEthernet-External-ME"  -NetAdapterName "Wi-Fi" -AllowManagementOS $true
```
<br/>

## Download Ubuntu Server ISO format
[https://ubuntu.com/download/server](https://ubuntu.com/download/server)

<br/>

## Install Virtual Machine From ISO
- Open Hyper-V Manager and Click Quick Create...  
![](https://github.com/EknarongAphiphutthikul/Hyper-V/blob/main/QuickCreate.png)
![](https://github.com/EknarongAphiphutthikul/Hyper-V/blob/main/SelectISO.png)

<br/>

## Add vEthernet-Internal-ME and vEthernet-External-ME to Virtual Machine
![](https://github.com/EknarongAphiphutthikul/Hyper-V/blob/main/AddInternalNetwork.png)
![](https://github.com/EknarongAphiphutthikul/Hyper-V/blob/main/AddExternalNetwork.png)

<br/>

## Check Your Current Kernel Version
```sh
uname –sr
```

<br/>

## Update the Repositories
```sh
sudo apt-get update
```

<br/>

## Set root password
```sh
sudo passwd root
```

<br/>

## Access To Root User
```sh
su -
```

<br/>

## Install Net tools
```sh
sudo apt install net-tools
```

<br/>

## Check Status ufw.service
```sh
sudo systemctl status ufw.service
```

<br/>

## Check status firewall
```sh
sudo ufw status
```

<br/>

## Enable your firewall
```sh
sudo ufw enable
```

<br/>

## Disable your firewall
```sh
sudo ufw disable
```

<br/>

## Set Default Policy firewall
```sh
sudo ufw default allow outgoing
sudo ufw default deny incoming
```

<br/>

## Allow ssh port
```sh
sudo ufw allow ssh
```

<br/>

## Reload ufw
```sh
sudo ufw reload
```

<br/>

## Show rule List
```sh
sudo ufw show listening
sudo ufw show added
```

<br/>

## View Firewall Log
```sh
sudo more /var/log/ufw.log
sudo tail -f /var/log/ufw.log
```