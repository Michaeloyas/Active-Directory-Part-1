# Active Directory Domain Services Part 1: VirtualBox, Virtual Machine(VM), Server and Client Installation, and Configuration

## Introduction
This is the first part of a series of home lab projects on setting up Active Directory Domain Services.

**Key learning aspects:**

* Downloading and installing VirtualBox and Extension.
* Download Microsoft Server 2019 ISO and Microsoft Windows 11 Operating System ISO.
* Installation of the server 2019 and the Windows 11 OS on virtual Machines (VM).

<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/3yTLVv7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

## Downloading and installing VirtualBox and Extension
Briefly, VirtualBox is a type 2 hypervisor. This means that it is installed on a host OS (unlike type 1, which is installed on bare metal) and enables you to spin up multiple environments (think of virtual machines) with different OSes (often called guest OSes).

Alright, to download VirtualBox, click on this [link](https://www.virtualbox.org/wiki/Downloads).

<br />
Select the disk:  <br/>
<img src="https://i.imgur.com/Jhcj0t7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Click to Download the option for your OS, download the extension pack, and save the download to a folder. We will be using the Windows OS for this exercise.

Once the download is completed, click on the file and follow the instructions in the Windows installer. Click “Next” until “Finish” to complete the installation. Next, click on the extension pack file to install it.

## Download Microsoft Server 2019 ISO and Microsoft Windows 11 Operating System ISO
To download the Microsoft Server 2019 ISO, click on this [link](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019) to download the 64-bit option.

To download the Windows 11 ISO, click on this [link](https://www.microsoft.com/en-us/software-download/windows11). Scroll down to Windows 11 ISO option => select the option for 64-bit in the dropdown box and click “Download Now” => select the preferred language in the dropdown and click “Confirm.”

A link will be generated for you to download the 64-bit option.

## Installation of the server 2019 and the Windows 11 OS on Virtual Machines (VM)
So far, we got the download part out of the way, and we are now ready to provision virtual machines and have the OSes installed on them to set the stage for the next fun part.

Open the VirtualBox you installed in the previous step and follow the steps below to launch a virtual machine.

1.  Click on the “New” option.

    * **Name:** Primary-DC // Domain Controller (DC) because we will install an active directory software on the server. Primary because, in production, more than one DC is recommended for redundancy. You’re free to name it anything.
    * **ISO Image:** Select the server 2019 you downloaded.
    * Other fields will automatically be populated. Leave the “Skip unattended installation” box unchecked, then click “Next”.

2.  Choose the credential (username and password) that you will use to log on to the server after boot up. Remember to check the “Guest Additions” box.

3.  Allocate base memory and processor based on your host hardware resources (RAM and CPU). Remember to stay within the green area of the bar.

4.  Select the “Create Virtual Hard Disk Now” and allocate the disk size. I decided to use 50 GB.

5.  Check the summary to be sure everything is okay, then click “Finish.”

    It will take a while to load files and then display the screen below:

6.  Click next and select one of the options with “Desktop Experience” to enable Graphical User Interface (GUI) on the server. Otherwise, it will just be command-line.

7.  Click “Next” => accept license agreement => Next => Click “custom install”.

8.  Click next, and the server will start to install. After a while, it will boot into Windows eventually.

9.  Set the credentials for the built-in administrator account.

10. Once you click “Finish,” it will boot up into the Windows GUI. Select “Input” => “Keyboard” => “Insert Ctrl-Alt-Del” to display the administrator and password field.

**Your turn!** Follow the steps above to launch a virtual machine and the Windows 11 ISO you downloaded.

## Summary
So far, you have downloaded and installed VirtualBox, provisioned virtual machines, and installed operating systems. That is quite a lot you have accomplished already! In the next part, we will configure our Domain Controller and do a lot more fun stuff.
