---
layout: default
---
# Using Wireshark to examine UDP and TCP Captures

## Environment
* This lab was carried out using the CyberOps VM workstation

## Part 1: Identify TCP Header Fields and Operation Using a Wireshark FTP Session Capture
### Starting a wireshark capture
* We first start wireshark using the command:

```
sudo wireshark-gtk &
```
* We then click on enp0s3 interface and then start to begin capturing packets
  
![enp0s3](./images/labs/Using_Wireshark_to_Examine_TCP_and_UDP_Captures/enp0s3.png)

### Connecting to FTP server
* We connect to an ftp server (ftp://test.rebex.net) using the following command:
```
sudo test.rebex.net
```
* Type in the command `ls` to view the files in the directory.
* Type in the command `get readme.txt` to retrieve the readme file.

![enp0s3](./images/labs/Using_Wireshark_to_Examine_TCP_and_UDP_Captures/ftp_sc1.png)

* We then close the connection and check our TCP / UDP packets.

### Viewing in wireshark
Setting the filter to `tcp and ip.addr == 194.108.117.16`

![enp0s3](./images/labs/Using_Wireshark_to_Examine_TCP_and_UDP_Captures/wireshark_tcp__filter_cap.png)
