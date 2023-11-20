# Intel_700_NIC_firmware_update
Steps to update Intel NIC firmware on Ubuntu (tested on Ubuntu 18.04)

1. Identify Ethernet Adapter and Firmware version by
```
   lspci | grep -i eth

   sudo ethtool -i eth5 # your nic interface name
```
2. Download the utility from Intel Website

   https://www.intel.com/content/www/us/en/download/18190/non-volatile-memory-nvm-update-utility-for-intel-ethernet-network-adapter-700-series.html

3. unzip the download and Linux version file
```
   tar xzvf 700Series_NVMUpdatePackage_v9_30_Linux.tar.gz
```
4. cd into the folder and start update
```
   cd 700Series/Linux_x64/

   sudo ./nvmupdate64e
```
5. select Adapter by Num and wait to finish

6. check updated NIC again
```
   sudo ethtool -i eth5
```
