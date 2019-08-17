### Connect RigCtrl to your WiFi

!!! attention ""
    RigCtrl device needs couple of minutes to startup for the first time!

1. From a mobile device or computer connect to **RigCtrlSetup** wireless
2. On a mobile device tap on **Sign In to network** notification when it appears
4. If you don't get the notification open [http://192.168.4.1](http://192.168.4.1?target=_blank) in your browser
5. Enter a name (which you will later use to get the local IP from [ip.rigctrl.com](https://ip.rigctrl.com?target=_blank))
6. Select your Wireless from the list and enter the password

!!! note ""
    Be patient until RigCtrl appears online

!!! error "If RigCtrlSetup wireless gets online again, it usually means that the password you entered was incorrect. Repeat instructions from step 1."
7. Open [ip.rigctrl.com](https://ip.rigctrl.com?target=_blank) and enter the name you provided during step 5. _It can take 1-2 minutes until the IP address apears_
8. Click on the IP address to continue with RigCtrl configuration

### Setup and update

1. Create user
2. Log in
3. Enter your wallet
4. If you have Premium subscription, enter email address and register to get Viber notifications
5. Click on the link to get the code for Viber
6. Enter credentials and information for Windows and Claymore
7. Save

!!! note ""
    Get latest updates and bug fixes by going to Updates in Menu

!!! attention "After saving configuration and updating, RigCtrl will start scanning the network for rigs. This operation takes couple of minutes before rigs start appearing."

### Windows configuration

_In order for RigCtrl to be able to install and configure Claymore, change wallets, restart Claymore and Windows, the Windows needs to be configured as bellow:_

1. Download **[config.zip](https://rigctrl.com/dl/config.zip?target=_blank)** in every rig
2. Extract the files by right clicking config.zip and click on Extract All...
3. From the new Windows Explorer right click on config.bat and click on Run as administrator
4. Enter information required by the script
5. In RigCtrl enter Windows user and password
    - Menu - Configuration - Windows configuration and save the changes

!!! important
    Windows user and password must to be the same on every rig!

### Claymore configuration

!!! note ""
    If you have completed [Windows Configuration](/installation/#windows-configuration) and have installed Claymore via RigCtrl, then you can skip this section.

To allow RigCtrl to perform action, Claymore needs to be configured with the following parameters:

- Add `-mport 3333` in your start.bat or config.txt
- Optionally you can add a password using `-mpsw password`
- Add `-r -1` to disable Claymore watchdog to not conflict with Rigctrl

!!! important
    Claymore port and password must to be the same on every rig!

!!! attention ""
    If you have choosen a different port than 3333 or password you have to update RigCtrl configuration. Menu - Configuration - Claymore Configuration and save the changes.

### SimpleMining configuration

1. Login in SimpleMining.net
2. Click on RigList -> OPTIONS: wallets -> Enter your wallet in Ethereum address ($walletETH) -> Click on Save all options and reload all rigs
3. Click on Rig Groups
4. Click Add group
5. Select Claymore version (recommended latest) by clicking on Select miner
6. Enter a group name, i.e. `RigCtrlGroup`
7. In Miner OPTIONS enter you configuration and modify or add `mport 3333`
    - Optionally you can add a password using `-mpsw password`
    - Example: `epool eu1.ethermine.org:4444 -ewal $walletETH.$rigName -esm 0 -epsw x -allpools 1 -mport 3333`
8. If you have entered your wallet in step 2. do not change `$walletETH`
9. Click on RigList
10. Select all rigs
11. Click ASSIGN GROUP
12. Select RigCtrlGroup (or name you entered in step 6.) and click Save.

!!! attention ""
    Enter the port and/or password in RigCtrl - Menu - Configuration - Claymore configuration and click save!