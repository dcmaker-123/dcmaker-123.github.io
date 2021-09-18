# What If I Forget the Passwords of S5700 Switches

As a hardware engineer, I found some particularly good learning materials during my work, which can help colleagues and communication beginners to better master the use methods and basic principles of network communication products. Among these learning materials, the quality and usability of Huawei TN are relatively high. Therefore, I will share with you some of the experience and learning experience of HW switch theme in the form of a column. If you are interested, you can combine these articles to learn.

Column: Excellent Switch Materials---Huawei ICT

【Chinese Version】

l RTU License of the switch Huawei S5700 switch

https://support.huawei.com/enterprise/zh/doc/EDOC1100191963

l Install the license for the switch stacking system, apply for loading, click merge

https://support.huawei.com/enterprise/zh/doc/EDOC1100191964

l Forgot the password of the switch Huawei S5700 switch

https://support.huawei.com/enterprise/en/doc/EDOC1100195306

【English Version】

l RTU Licenses for HW S5700 Switches

https://support.huawei.com/enterprise/en/doc/EDOC1100195306

l How to Install a License for a Stack System of S Series Switches

https://support.huawei.com/enterprise/en/doc/EDOC1100195305

l What If I Forget the Passwords of HW S5700 Switches:

https://support.huawei.com/enterprise/en/doc/EDOC1100195306

 

[Introduction. 1](#_Toc81405508)

[Prerequisites 1](#_Toc81405509)

[Scenario 1: All Default Passwords Are Changed and All Passwords Are Forgotten. 2](#_Toc81405510)

[Scenario 2: Default Passwords Are Forgotten. 2](#_Toc81405511)

[Scenario 3: The Console Port Login Password Is Forgotten. 3](#_Toc81405512)

[Method 1: Log in to the device using STelnet or Telnet and change the console port login password. 3](#_Toc81405513)

[Method 2: Clear the console port login password in the BootROM/BootLoad menu and change the console port login password. 5](#_Toc81405514)

[Scenario 4: The STelnet/Telnet Login Password Is Forgotten. 7](#_Toc81405515)

[Method 1: Use an STelnet/Telnet Account with Administrator Rights to Log In to the Device and Reset the Password 7](#_Toc81405516)

[Method 2: Log In to the Device Through the Console Port and Set a New STelnet/Telnet Login Password 11](#_Toc81405517)

[Scenario 5: The BootROM/BootLoad Password Is Forgotten but the Console Port/STelnet/Telnet Login Is Available 12](#_Toc81405518)

[Changing the BootROM Password. 13](#_Toc81405519)

[Changing the BootLoad Password. 14](#_Toc81405520)

[Scenario 6: The Web Login Password Is Forgotten but the Console Port/STelnet/Telnet Login Is Available 15](#_Toc81405521)

## Introduction

Have you ever forgotten the switch passwords? Have you ever failed to log in to your switch because of a lost login password?

This document describes how to clear the old password or set a new password when you forget the console port login password, STelnet/Telnet login password, BootROM/BootLoad password, or web login password. This ensures that you can log in to your switch even when you forget these passwords.

For details about how to log in to a switch, see [Switches Typical Login Configuration Examples](https://support.huawei.com/enterprise/zh/doc/EDOC1000069491/176653a6).

## Prerequisites

This document uses S series switches of V200R020C00 as an example to describe how to clear the old password or set a new password. The operations to be performed may vary depending on the device model and version. For details, see the corresponding product documentation.

This document is written based on device information obtained under lab conditions. If your device is running on the live network, ensure that you understand the potential impact of all commands.

## Scenario 1: All Default Passwords Are Changed and All Passwords Are Forgotten

If you change all default passwords and forget the console port login password, all STelnet/Telnet login accounts and passwords, and BootROM/BootLoad passwords:

·     For a switch that has the PNP button, you can press and hold the PNP button for more than 6 seconds to restore the switch to factory settings and restart the switch. The following figure shows the PNP button.

·     If the switch does not have the PNP button, return it to the factory for repair.

**Figure 1-1** PNP button
 ![https://download.huawei.com/mdl/image/download?uuid=0aed538a110c413099373e78441846cd](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image002.png)

For details about mandatory configurations of the switch after factory settings are restored, see [Restoring the Factory Settings of S5700 Series Switches](https://support.huawei.com/enterprise/en/doc/EDOC1100088109/43c29a66?idPath=24030814|21782164|21782167|22318564|6691579).

**![https://download.huawei.com/mdl/image/download?uuid=190a83cc20d64a0293817026f3f018a0](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image003.png)**

After factory settings are restored, all configuration data is deleted and cannot be restored. Therefore, exercise caution when restoring the factory settings of the switch.

## Scenario 2: Default Passwords Are Forgotten

For S series switches running V200R020 and later versions, no passwords are configured for default accounts, and users must configure new passwords for logging in to the switches. In this situation, scenario 2 is not involved.

However, for S series switches running versions earlier than V200R020, there is no default STelnet/Telnet login password, but there are default console port login password, default BootROM/BootLoad password, and default web login password. These default passwords may vary according to the switch version.

If you always use the default passwords and have not changed the passwords, you can obtain the default accounts and passwords according to **S Series Switches Default Usernames and Passwords** (for [enterprise users](https://support.huawei.com/enterprise/en/doc/EDOC1100182397/bd7ca1e4?idPath=24030814|21782164|21782167|22318635|6691602) or [carrier users](https://support.huawei.com/carrier/docview!docview?nid=DOC1100768677)). The permission level of this document is C (customer support level). If you need to upgrade the permission level, see the help document on the website.

![https://download.huawei.com/mdl/image/download?uuid=b60a5c1e99704fc8996c8c3e558f4ba0](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

To ensure device security, you are advised not to use the default passwords and to change the passwords periodically.

## Scenario 3: The Console Port Login Password Is Forgotten

Three methods are available to recover the console port login password.

·     Method 1: [Log in to the device using STelnet or Telnet and change the console port login password.](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#section16636144275418)

·     Method 2: [Clear the console port login password in the BootROM/BootLoad menu and change the console port login password.](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#section1612361212554)

![https://download.huawei.com/mdl/image/download?uuid=b60a5c1e99704fc8996c8c3e558f4ba0](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

Method 1 is recommended. Use method 2 if you also forget the STelnet or Telnet login password. STelnet V2 is recommended because it is more secure than Telnet.

### Method 1: Log in to the device using STelnet or Telnet and change the console port login password.

If you have an STelnet or Telnet account and administrator permissions, you can log in to the device through STelnet or Telnet, change the console port login password, and save the configuration.

The following describes how to change the console port login password after logging in to the device using STelnet.

\1.    Use the STelnet account to log in to the device and ensure that the account has a privilege level of 3 or higher.

Run the **display users** command to check all the users who have logged in to the device. The line marked with a plus sign (+) indicates the current user. Record the **User-Intf** field value (**VTY1**).

```
<HUAWEI> display users 
  User-Intf    Delay    Type   Network Address     AuthenStatus    AuthorcmdFlag 
  129 VTY 0   00:23:36  TEL    10.135.18.67              pass           no        Username : Unspecified 
 
+ 130 VTY 1   01:20:36  SSH    10.135.18.91              pass           no        Username : Unspecified 
 
  131 VTY 2   00:00:00  TEL    10.135.18.54              pass           no        Username : Unspecified
```

Run the **display user-interface** command to check the permissions of all users. The command output shows that the privilege level of VTY1 is 15, which has the right to change the console port login password.

```
<HUAWEI> display user-interface 
  Idx  Type     Tx/Rx      Modem Privi ActualPrivi Auth  Int 
  0    CON 0    9600       -     15    -           P     - 
+ 129  VTY 0               -     15    15          P     - 
+ 130  VTY 1               -     15    15          P     - 
+ 131  VTY 2               -     15    -           P     - 
  132  VTY 3               -     15    15          P     - 
......
```

\2.    Change the console port login password.

§ The following example changes the authentication mode to password authentication and the password to **test@123**.

```
<HUAWEI> system-view 
[HUAWEI] user-interface console 0 
[HUAWEI-ui-console0] authentication-mode password 
[HUAWEI-ui-console0] set authentication password cipher test@123
[HUAWEI-ui-console0] return
```

§ The following example changes the authentication mode to AAA authentication, user name to **admin123**, and password to **test@123**.

```
<HUAWEI> system-view 
[HUAWEI] user-interface console 0 
[HUAWEI-ui-console0] authentication-mode aaa
[HUAWEI-ui-console0] quit
[HUAWEI] aaa
[HUAWEI-aaa] local-user admin123 password irreversible-cipher test@123
[HUAWEI-aaa] local-user admin123 service-type terminal
[HUAWEI-aaa] return
```

\3.    To prevent configuration loss after a device restart, save the device configuration.

```
<HUAWEI> save 
The current configuration will be written to the device. 
Are you sure to continue?[Y/N]y 
Now saving the current configuration to the slot 0. 
Save the configuration successfully.
```

### Method 2: Clear the console port login password in the BootROM/BootLoad menu and change the console port login password.

If you remember the BootROM/BootLoad password and can access the BootROM/BootLoad menu, clear the console port login password in the BootROM/BootLoad menu, set a new console port login password after the device restarts, and save the configuration.

**![https://download.huawei.com/mdl/image/download?uuid=190a83cc20d64a0293817026f3f018a0](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image003.png)**

·     To access the BootROM/BootLoad menu, you need to restart the device. You can power off and then power on the device to restart it. This operation, however, will interrupt services and may cause the loss of configuration and data. Perform this operation during off-peak hours. Do not power off the device when the device starts.

·     For a modular switch with dual MPUs, remove the standby MPU before restarting the switch. Perform the following operations, install the standby MPU and run the **save** command to ensure that the configurations on the active and standby MPUs are the same.

·     If multiple switches are stacked, power off these member switches. Perform the following operations on the master switch, and run the **save** command to ensure that the configurations on the master switch can be synchronized to other member switches after other member switches start up.

·     If there is no COM port (DB9 serial port) on your maintenance terminal (PC), purchase a DB9-to-USB cable to connect the USB port to the maintenance terminal.

Perform the following operations.

\1.    Connect the PC to the switch through the console port on the switch. Connect the DB9 female connector of the console cable to the COM port on the PC, and connect the RJ45 connector to the console port on the switch, as shown in [Figure 1-2](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#fig208637061320).

**Figure 1-2** Connecting a PC to the switch through the console port on the switch
 ![https://download.huawei.com/mdl/image/download?uuid=254dbe6da17c47e5b8d66f7bc76f8e21](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image006.png)

\2.    Start the terminal emulation software on the PC. Create a connection, select the connection port, and set communication parameters:

§ Baud rate: 9600

§ Data bits: 8

§ Stop bits: 1

§ Parity: None

§ Flow control: None

\3.    Restart the switch. When the following message is displayed, press **Ctrl+B** or **Ctrl+E** immediately and enter the password to enter the BootROM/BootLoad menu.

```
Press Ctrl+B or Ctrl+E to enter BootROM/BootLoad menu ... 2
password:      //Enter the BootROM/BootLoad password.
```

![https://download.huawei.com/mdl/image/download?uuid=b60a5c1e99704fc8996c8c3e558f4ba0](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

§ The output varies according to the device and version. Therefore, the output on your device may be different from that provided in this example.

§ If you have not changed the default BootROM/BootLoad password, enter the default password to access the BootROM/BootLoad main menu. You can obtain the default accounts and passwords according to **S Series Switches Default Usernames and Passwords** (for [enterprise users](https://support.huawei.com/enterprise/en/doc/EDOC1100182397/bd7ca1e4?idPath=24030814|21782164|21782167|22318635|6691602) or [carrier users](https://support.huawei.com/carrier/docview!docview?nid=DOC1100768677)). The permission level of this document is C (customer support level). If you need to upgrade the permission level, see the help document on the website.

\4.    Select **Clear password for console user** on the BootROM/BootLoad menu to clear the console port login password.

\5.    Select **Boot with default mode** on the BootROM/BootLoad menu to start the switch as prompted.

**![https://download.huawei.com/mdl/image/download?uuid=ee900806996e4540842714a741fa7d66](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image007.png)**

Do not select **Reboot**; otherwise, the password cannot be cleared.

\6.    After the switch starts, authentication is not required when you log in to the switch through the console port. Set a password as prompted after the login. In V200R009 and later versions, after the switch starts up, the authentication mode for a console port login is non-authentication, and the system does not ask you to configure an authentication password.

\7.    After logging in to the switch, set an authentication mode and password for the console user interface according to service requirements. For details about how to change the console port login password, see [Step 2](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#li39121828142012) in Method 1.

\8.    To prevent configuration loss after a device restart, save the device configuration.

```
<HUAWEI> save 
The current configuration will be written to the device. 
Are you sure to continue?[Y/N]y 
Now saving the current configuration to the slot 0. 
Save the configuration successfully.
```

## Scenario 4: The STelnet/Telnet Login Password Is Forgotten

·     If you forget the login password of an STelnet/Telnet account, you can use another STelnet/Telnet account with administrator rights to log in to the device and reset the password. For details, see [Method 1](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#section15795647152216).

·     If you forget the passwords of all STelnet/Telnet accounts but can log in to the device through the console port, see [Method 2](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#section02811912121818).

### Method 1: Use an STelnet/Telnet Account with Administrator Rights to Log In to the Device and Reset the Password

\1.    Log in to the switch using the STelnet/Telnet account with administrator rights.

\2.    Change the STelnet/Telnet login password. The following example describes how to change the STelnet/Telnet login password of VTY0 to VTY4.

**Table 1-1** Changing the STelnet/Telnet login password

| **Password Change   Scenario**                               | **Configuration**                                            |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| Set the Telnet  login authentication mode to password authentication, password to **test@123**,  and user privilege level to 15. | `<HUAWEI> **system-view**``[HUAWEI] **user-interface vty 0** **4**``[HUAWEI-ui-vty0-4] **protocol inbound telnet**  //By default, switches running V200R006 and earlier versions use Telnet and do not need to have this command configured; switches running V200R007 and later versions use SSH and need to have this command configured.``[HUAWEI-ui-vty0-4] **authentication-mode password**``[HUAWEI-ui-vty0-4] **set authentication password cipher test@123**``[HUAWEI-ui-vty0-4] **user privilege level 15**``[HUAWEI-ui-vty0-4] **return**``<HUAWEI> **save**` |
| Set the Telnet  login authentication mode to AAA authentication, user name to **testuser**,  password to **test@123**, and user privilege level to 15.  If  the user name is the original one, you can reset the password of the original  login account. If the user name is a new one, you can configure a new Telnet  login account. The configuration methods in the two scenarios are the same. | `<HUAWEI> **system-view**``[HUAWEI] **user-interface vty 0** **4**``[HUAWEI-ui-vty0-4] **protocol inbound telnet**  //By default, switches running V200R006 and earlier versions use Telnet and do not need to have this command configured; switches running V200R007 and later versions use SSH and need to have this command configured.``[HUAWEI-ui-vty0-4] **authentication-mode aaa**``[HUAWEI-ui-vty0-4] **quit** ``[HUAWEI] **aaa** ``[HUAWEI-aaa] **local-user testuser password irreversible-cipher test@123** ``[HUAWEI-aaa] **local-user huawei service-type telnet** ``[HUAWEI-aaa] **local-user huawei privilege level 15**``Warning: This operation may affect online users, are you sure to change the user privilege level ?[Y/N]**y**``[HUAWEI-aaa] **return**``<HUAWEI> **save**` |
| Set the STelnet  login authentication mode to password authentication, user name to **admin123**,  password to **abcd@123**, and user privilege level to 15.  If  the user name is the original one, you can reset the password of the original  login account. If the user name is a new one, you can configure a new STelnet  login account. The configuration methods in the two scenarios are the same. | `<HUAWEI> **system-view**``[HUAWEI] **user-interface vty 0** **4**``[HUAWEI-ui-vty0-4] **protocol inbound ssh**  //By default, switches running V200R006 and earlier versions use Telnet and need to have this command configured. Switches running V200R007 and later versions use SSH and do not need to have this command configured.``[HUAWEI-ui-vty0-4] **authentication-mode aaa**``[HUAWEI-ui-vty0-4] **user privilege level 15**``[HUAWEI-ui-vty0-4] **quit** ``[HUAWEI] **ssh user admin123**``[HUAWEI] **ssh user admin123 service-type stelnet**``[HUAWEI] **ssh user admin123 authentication-type password**``[HUAWEI] **aaa** ``[HUAWEI-aaa] **local-user admin123 password irreversible-cipher abcd@123** ``[HUAWEI-aaa] **local-user admin123 privilege level 15**``[HUAWEI-aaa] **local-user admin123 service-type ssh**``[HUAWEI-aaa] **quit**``[HUAWEI] **ecc local-key-pair create** ``Info: The key name will be: HUAWEI_Host_ECC. Info: The key modulus can be any one of the following: 256, 384, 521. Info: If the key modulus is greater than 512, it may take a few minutes. Please input the modulus [default=521]:**521** ``Info: Generating keys.......... ``Info: Succeeded in creating the ECC host keys.``[HUAWEI] **return**``<HUAWEI> **save**` |
| Set the STelnet  login authentication mode to ECC authentication (similar to RSA or DSA  authentication), user name to **admin123**, password  to **abcd@123**, and user privilege level to 15.  If  the user name is the original one, you can reset the password of the original  login account. If the user name is a new one, you can configure a new STelnet  login account. The configuration methods in the two scenarios are the same.  To  use ECC authentication, you need to configure the public key of the SSH  client on the SSH server. When the SSH client connects to the SSH server, the  SSH client passes the authentication if the private key of the client matches  the configured public key. For details about the public key on the SSH  client, see the help document of the SSH client software. | `<HUAWEI> **system-view**``[HUAWEI] **user-interface vty 0** **4**``[HUAWEI-ui-vty0-4] **protocol inbound ssh**  //By default, switches running V200R006 and earlier versions use Telnet and need to have this command configured. Switches running V200R007 and later versions use SSH and do not need to have this command configured.``[HUAWEI-ui-vty0-4] **authentication-mode aaa**``[HUAWEI-ui-vty0-4] **user privilege level 15**``[HUAWEI-ui-vty0-4] **quit** ``[HUAWEI] **ssh user admin123**``[HUAWEI] **ssh user admin123 service-type stelnet**``[HUAWEI] **ssh user admin123 authentication-type ecc**``[HUAWEI] **ecc peer-public-key key01 encoding-type pem** ``Enter "ECC public key" view, return system view with "peer-public-key end". ``[HUAWEI-ecc-public-key] **public-key-code begin**  //Enter the public key editing view.``Enter "ECC key code" view, return last view with "public-key-code end".``[HUAWEI-dsa-key-code] **308188**  //Copy the public key of the client, which is a hexadecimal character string.``[HUAWEI-dsa-key-code] **028180**``[HUAWEI-dsa-key-code] **B21315DD 859AD7E4 A6D0D9B8 121F23F0 006BB1BB**``[HUAWEI-dsa-key-code] **A443130F 7CDB95D8 4A4AE2F3 D94A73D7 36FDFD5F**``[HUAWEI-dsa-key-code] **411B8B73 3CDD494A 236F35AB 9BBFE19A 7336150B**``[HUAWEI-dsa-key-code] **40A35DE6 2C6A82D7 5C5F2C36 67FBC275 2DF7E4C5**``[HUAWEI-dsa-key-code] **1987178B 8C364D57 DD0AA24A A0C2F87F 474C7931**``[HUAWEI-ecc-key-code] **A9F7E8FE E0D5A1B5 092F7112 660BD153 7FB7D5B2**``[HUAWEI-ecc-key-code] **171896FB 1FFC38CD**``[HUAWEI-ecc-key-code] **0203**``[HUAWEI-ecc-key-code] **010001**``[HUAWEI-ecc-key-code] **public-key-code end**   //Return to the public key view.``[HUAWEI-ecc-public-key] **peer-public-key end**  //Return to the system view.``[HUAWEI] **ssh user admin123 assign ecc-key key01**  //Assign an existing public key **key01** to user **admin123**.``[HUAWEI] **ecc local-key-pair create** ``Info: The key name will be: HUAWEI_Host_ECC. Info: The key modulus can be any one of the following: 256, 384, 521. Info: If the key modulus is greater than 512, it may take a few minutes. Please input the modulus [default=521]:**521** ``Info: Generating keys.......... ``Info: Succeeded in creating the ECC host keys.``[HUAWEI] **return**``<HUAWEI> **save**` |

### Method 2: Log In to the Device Through the Console Port and Set a New STelnet/Telnet Login Password

If you forget the STelnet/Telnet login password but remember the console port login password, log in to the switch through the console port and set a new STelnet/Telnet login password.

![https://download.huawei.com/mdl/image/download?uuid=b60a5c1e99704fc8996c8c3e558f4ba0](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

STelnet V2 is recommended because it is more secure than Telnet.

\1.    Connect the PC to the switch through the console port on the switch. Connect the DB9 female connector of the console cable to the COM port on the PC, and connect the RJ45 connector to the console port on the switch, as shown in [Figure 1-2](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#fig208637061320).

**Figure 1-3** Connecting a PC to the switch through the console port on the switch
 ![https://download.huawei.com/mdl/image/download?uuid=254dbe6da17c47e5b8d66f7bc76f8e21](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image009.png)

\2.    Start the terminal emulation software on the PC. Create a connection, select the connection port, and set communication parameters:

§ Baud rate: 9600

§ Data bits: 8

§ Stop bits: 1

§ Parity: None

§ Flow control: None

\3.    Click **Connect**. Enter or configure the login password as prompted to log in to the switch through the console port.

\4.    Change the STelnet/Telnet login password. For details, see [Step 2](https://support.huawei.com/enterprise/en/doc/EDOC1100200698#li931019118235) in Method 1.

## Scenario 5: The BootROM/BootLoad Password Is Forgotten but the Console Port/STelnet/Telnet Login Is Available

If you can log in to the switch through the console port, STelnet, or Telnet, log in to the switch and restore the default BootROM/BootLoad password. You can obtain the default accounts and passwords according to **S Series Switches Default Usernames and Passwords** (for [enterprise users](https://support.huawei.com/enterprise/en/doc/EDOC1100182397/bd7ca1e4?idPath=24030814|21782164|21782167|22318635|6691602) or [carrier users](https://support.huawei.com/carrier/docview!docview?nid=DOC1100768677)). The permission level of this document is C (customer support level). If you need to upgrade the permission level, see the help document on the website.

```
<HUAWEI> reset boot password
The password used to enter the boot menu by clicking Ctrl+B will be restored to the default password, continue? [Y/N] y
```

![https://download.huawei.com/mdl/image/download?uuid=b60a5c1e99704fc8996c8c3e558f4ba0](file:///C:\Users\G50020~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

To ensure device security, you are advised not to use the default passwords and to change the passwords periodically.

### Changing the BootROM Password

To change the BootROM password, you need to restart the device and access the BootROM main menu.

\1.    Restart the device.

```
<HUAWEI> reboot 
Info: The system is now comparing the configuration, please wait........ 
Warning: The configuration has been modified, and it will be saved to the next startup saved-configuration file flash:/204.cfg. Continue? [Y/N]:y
Info: If want to reboot with saving diagnostic information, input 'N' and then execute 'reboot save diagnostic-information'.                                    System will reboot! Continue?[Y/N]:y
```

\2.    When the message "Press Ctrl+B or Ctrl+E to enter BootROM menu:" is displayed, press **Ctrl+B** or **Ctrl+E** within 3 seconds, and enter the default password to access the BootROM main menu.

In the BootROM main menu, select 6 to access the password submenu.

```
          BootROM  MENU
 1. Boot with default mode
    2. Enter serial submenu
    3. Enter startup submenu
    4. Enter ethernet submenu
    5. Enter filesystem submenu
    6. Enter password submenu
    7. Clear password for console user
    8. Reboot
    (Press Ctrl+E to enter diag menu) 
 
Enter your choice(1-8):6
 
 
        PASSWORD  SUBMENU
 
     1. Modify bootload password
     2. Reset bootload password
     3. Return to main menu
 
Enter your choice(1-3):
```

\3.    In the password submenu, select 1 to change the BootROM password.

```
       PASSWORD  SUBMENU
    1. Modify BootROM password
2. Reset BootROM password
3. Return to main menu
Enter your choice(1-3): 1
Old password:     //Enter the old password.
New password:     //Enter a new password.
Verify:           //Enter the new password again.
```

### Changing the BootLoad Password

To change the BootLoad password, you need to restart the device and access the BootLoad main menu.

\1.    Restart the device.

```
<HUAWEI> reboot 
Info: The system is now comparing the configuration, please wait........ 
Warning: The configuration has been modified, and it will be saved to the next startup saved-configuration file flash:/204.cfg. Continue? [Y/N]:y  Info: If want to reboot with saving diagnostic information, input 'N' and then execute 'reboot save diagnostic-information'.                                    System will reboot! Continue?[Y/N]:y
```

\2.    When the message "Press Ctrl+B or Ctrl+E to enter BootLoad menu:" is displayed, press **Ctrl+B** or **Ctrl+E** within 3 seconds, and enter the default password to access the BootLoad main menu.

In the BootLoad main menu, select 5 to access the password submenu.

```
        BootLoad Menu                                                                                                                                           
     1. Boot with default mode                                                  
     2. Enter startup submenu                                                   
     3. Enter ethernet submenu                                                  
     4. Enter filesystem submenu                                                
     5. Enter password submenu                                                  
     6. Clear password for console user                                         
     7. Reboot                                                                  
    (Press Ctrl+E to enter diag menu)                                           
                                                                           
Enter your choice(1-7):5
        PASSWORD  SUBMENU
     1. Modify bootload password
     2. Reset bootload password
     3. Return to main menu
Enter your choice(1-3):
```

\3.    In the password submenu, select 1 to change the BootLoad password.

```
        PASSWORD  SUBMENU
     1. Modify bootload password
     2. Reset bootload password
     3. Return to main menu
Enter your choice(1-3): 1
Old password:     //Enter the old password.
New password:     //Enter a new password.
Verify:           //Enter the new password again.
```

## Scenario 6: The Web Login Password Is Forgotten but the Console Port/STelnet/Telnet Login Is Available

If you can log in to the switch through the console port, STelnet, or Telnet, log in to the switch and reset the web login password. In the following example, the web login user name is **admin123** and the password is **test@123**.

```
<HUAWEI> system-view
[HUAWEI] aaa
[HUAWEI-aaa] local-user admin123 password irreversible-cipher test@123
[HUAWEI-aaa] local-user admin123 service-type http
[HUAWEI-aaa] local-user admin123 privilege level 15
Warning: This operation may affect online users, are you sure to change the user privilege level ?[Y/N]y
[HUAWEI-aaa] return
<HUAWEI> save
```

 

**For more reference resources, please click to enter (ebook) CloudCampus 3.0 Solution**

https://support.huawei.com/enterprise/en/doc/EDOC1100201111

 
