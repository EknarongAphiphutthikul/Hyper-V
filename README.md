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