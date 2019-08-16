### Managing groups for installing and configuring Claymore

!!! info ""
    RigCtrl Claymore operations are available only if Windows configuration guide is completed

Usually the rigs share together most of the Claymore parameters like wallet, fan speed settings, pool, etc. You want to keeps those commong parameters in a group and use it in all or a group of rigs.

_RigCtrl has a default `global` group with predefined Claymore parameters that rigs will initially use_

To add a group click on +

1. Enter group name

    !!! info "Example"
        Name could be a group for rigs with same cards `RX580-8GB` or `RX570-4GBSapphire`

2. Enter wallet only if it's different from the wallet in gray (wallet in Configuration) or you want a group that will mine for another wallet

3. In Claymore command enter the complete command (except wallet). Refer to **[Claymore documentation](https://www.rigctrl.com/dl/readme.txt?target=_blank)** for available options.

!!! info ""
    Default RigCtrl global command is `-epool eu1.ethermine.org:4444 -cvddc 900 -cclock 1150 -mclock 2000 -tstop 85 -tt 60 -fanmin 35 -fanmax 100 -r -1 -mport 3333`

If a rig has different mclock, cclock or cvddc than other rigs in the same group, they can be entered and overriden by entering those in the rig list.

If a rig needs different commands other than overclocking then create a new group for that rig.

### Managing rigs

1. To manage rigs click on Rig/Group list from the menu
2. Add a rig by clicking on **+** or remove a rig with **X**
3. Change rig name for easier identification
4. Enter or adjust Min hashrate

    !!! attention ""
        Minimal hashrate is the lower boundary where if rig drops below that hashrate RigCtrl acts and restarts Claymore, Windows or perform a reset to bring the rig to optimal hashrate.

        It is important to enter correct min hashrate to have RigCtrl help you the best way.

5. Select reset Port where rig is connected to. If a rig doesn't have assigned port it is not possible to hard reset, power off or power on.
6. Select appropriate group
7. Monitoring
    - If a rig has Monitor selected, RigCtrl will monitor the rig and automatically peform actions like Claymore/Windows restart or hard reset.
    - Uncheck monitoring if you don't want RigCtrl to take actions on a  rig.
    - Monitoring can be turned on or off from the home page as well.
    - Regardless of monitoring, manual actions can be pefromed from the home page.


### Installing and configuring Claymore

1. Enter `cvddc`, `mclock` and/or `cclock` that are specific to a rig in respecive fields in the list

    !!! info "Example"
        A rig has different GPUs and require different clocks than in group. We enter the following:

        cvddc: 950

        cclock: 1150,1150,1130,1120,1140,1050

        mclock: 2050,2050,2000,1900,2040,2050

    !!! attention ""
        The final Claymore command will be the group's commands except the clocks entered in the rig.

2. Click on green play button to install or update Claymore
    - This action installs/updates, combines group parameters with rig's clock, configures Claymore and puts Claymore in Windows startup
    - Claymore version is always the latest
3. Click on refresh button to send new Claymore configuration if any of the global or rig parameters are changed.
    - This action only changes the Claymore command

!!! Warning
    Save the changes before executing any of the actions

### Managing rigs from the home page

On home page every rig has its own menu where you can manage and take different actions

- Click on three vertical dots to open rig menu
    - Edit Rig - From this dialog you can change rig information, claymore configuration and perform various actions
    - Teamviewer ID - appears only if Teamviewer is installed on rig (click to copy ID)
    - Restart Claymore
    - Monitor On/Off
    - Windows Restart
    - Windows Shutdown

    _The commands below are ony available if a rig is connected to a RigCtrl Reset device and has a port assigned_
    - Reset
    - Power off
    - Power on

