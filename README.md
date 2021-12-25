# ISLAMIC DIGITAL COIN Masternode Setup (Ubuntu OS)
This guide will assist you in setting up a ISLAMIC DIGITAL COIN Masternode on a Linux Server running Ubuntu OS


***
- [ISLAMIC DIGITAL COIN Masternode Setup](#islamic-digital-coin-masternode-setup)  
  	* [Requirements](#requirements) 
  * [Connecting to the VPS and installing the masternode script](#Connecting-to-the-VPS-and-installing-the-masternode-script)  
         [1. Log into the VPS with **root**](#1-log-into-the-vps-with-root)  
         [2. Git Installation](#2-git-installation)  
         [3. Clone MN setup script](#3-clone-mn-setup-script)  
         [4. Start MN setup script](#4-start-mn-setup-script)  
         [5. Now ask for VPS Public IP Address](#5-now-ask-for-vps-public-ip-address)  
         [6. Copy Masternode Private Key](#6-copy-masternode-private-key-from-vps-console-window-and-pres-enter)
  * [Setup QT wallet](#setup-qt-wallet)  
         [1. Create new receiving address and copy it](#1-create-new-receiving-address-and-copy-it)  
	 [2. Send 10,000 ISLAMIC DIGITAL COIN to copied address](#2-send-10000-islamic-digital-coin-cash-to-copied-address)  
	 [3. Get MN output and Set Masternode Configuration File](#3-open-console-get-mn-output-and-set-masternode-configuration-file-and-save-it)  
	 [4. Wait at least 15 confirmation of transaction](#4-wait-at-least-15-confirmation-of-transaction)  
         [5. Restart QT wallet](#5-restart-qt-wallet)  
         [6. Start MN in QT wallet console](#6-start-mn-in-qt-wallet-console)  
	 [7. Check Masternode Status in VPS](#7-check-masternode-status-in-vps)  

***
## Requirements
- 10,000 ISLAMIC DIGITAL COIN.
- A VPS running Linux Ubuntu OS with 1 CPU & 1GB Memory minimum (2gb Recommended) from [Vultr](https://www.vultr.com/?ref=8622028) or any other providers.
- ISLAMIC DIGITAL COIN Wallet (Local Wallet)
- An SSH Client (<a href="https://www.putty.org/" target="_blank">Putty</a> or <a href="https://dl.bitvise.com/BvSshClient-Inst.exe" target="_blank">Bitvise</a>)

***
## Connecting to the VPS and installing the masternode script
***
##### 1. Log into the VPS with **root**  
[![Vps](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/1.png)]
***
##### 2. Git Installation:  
- ```sudo apt-get install -y git-core```  

[![Git](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/2.png)]
***
##### 3. Clone MN setup script: 
- ```git clone https://github.com/ISLAMIC-DIGITAL-COIN/IDC-MN.git```  

[![Script1](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/3.png)] 
***
##### 4. Start MN setup script: 
- ```cd IDC-MN && chmod +x ./IDC-MN.sh && ./IDC-MN.sh```  
   
[![Script2](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/4.png)]  

##### 5. Now ask for VPS Public IP Address
[![Script3](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/5.png)]

**Now you need to wait some time, while script preparing the VPS to setup**  
***
##### 6. Copy masternode private key from VPS console window and pres "Enter":
[![Download Bitvise](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/6.png)] 

- if you see this, you are on the right track:
[![QT1](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/7.png)]

- to check VPS daemon status, type: ```islamic_digital_coin-cli  getinfo```
[![QT2](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/8.png)]

**Don't close this window!** 
***		

## Setup QT wallet
##### 1. Create new receiving address and copy it
[![QT3](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/9.png)] 

***
##### 2. Send 10,000 ISLAMIC DIGITAL COIN to copied address
[![QT4](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/10.png)]
***
##### 3. Open console Get MN output and set masternode configuration file and save it
- ```mn1 VPS_IP:17151 masternode_genkey masternode_output output_index```:
[![QT5](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/11.png)]
***
##### 4. Wait at least 15 confirmation of transaction
[![QT6](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/12.png)]
***
##### 5. Restart QT wallet  
- **it's important**
***
##### 6. Start MN in QT wallet console:
- ```startmasternode alias false TEST-MN```

[![QT7](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/13.png)]
***
##### 7. Check Masternode Status in VPS:
- ```islamic_digital_coin-cli startmasternode local false``` 
- ```islamic_digital_coin-cli getmasternodestatus```  
[![QT8](https://raw.githubusercontent.com/ISLAMIC-DIGITAL-COIN/IDC-MN/master/assets/14.png)]  
***
**Сongratulations you did it!**