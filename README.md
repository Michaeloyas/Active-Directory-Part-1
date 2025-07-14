# Active Directory Domain Services Part 1: VirtualBox, Virtual Machine (VM), Server 2019 and Windows 11 Installation, and Configuration

## Introduction
This is the first part of a series of home lab projects on setting up Active Directory Domain Services.

**Key learning aspects:**

* Virtualization: Hypervisor (Oracle VirtualBox) download and installation.
* Software Installation: Microsoft Server 2019 ISO and Microsoft Windows 11 Operating System ISO mounting and installation on virtual machines.

![Active Directory implementation chart](https://i.imgur.com/3yTLVv7.png)


## Downloading and installing VirtualBox and Extension Pack
Briefly, VirtualBox is a type 2 hypervisor. This means that it is installed on a host OS (unlike type 1, which is installed on bare metal) and enables you to spin up multiple environments (think of virtual machines) with different OSes (often called guest OSes).

Here is the download [link](https://www.virtualbox.org/wiki/Downloads).

<br />
VirtualBox download Steps:  <br/>
<img src="https://i.imgur.com/Jhcj0t7.png" height="40%" width="80%" alt="VirtualBox download"/>
<br />
<br />

I downloaded the option for Windows OS and the extension pack, and saved the download to a folder.

Once the download is completed, click on the file and follow the instructions in the Windows installer. Click “Next” until “Finish” to complete the installation. Next, click on the extension pack file to install it.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*l1qBKOBKbBDafxlr5U_5lg.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

## Download Microsoft Server 2019 ISO and Microsoft Windows 11 Operating System ISO
To download the Microsoft Server 2019 ISO, click on this [link](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019) to download the 64-bit option.

To download the Windows 11 ISO, click on this [link](https://www.microsoft.com/en-us/software-download/windows11). Scroll down to Windows 11 ISO option => select the option for 64-bit processor in the dropdown box and click “Download Now” => select the preferred language in the dropdown and click “Confirm.”

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*lk5e1E--f_7E9dk0oSLf-g.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

A link will be generated for you to download the 64-bit option.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*P1mn4JPVjKgjg-t1V_iAtA.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

## Installation of the server 2019 and the Windows 11 OS on Virtual Machines (VM)
So far, we got the download part out of the way, and we are now ready to provision virtual machines and have the OSes installed on them to set the stage for the next fun part.

Open the VirtualBox you installed in the previous step and follow the steps below to launch a virtual machine.

1.  Click on the “New” option.

<br />
<img src="https://cdn-images-1.medium.com/max/1200/1*0v0oN704tceYseUPV7kJLw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

* **Configure Virtual Machine Details**
    * **Name:**
        ~ Primary-DC. This will be our Domain Controller (DC) since we're installing Active Directory software on it. We're naming it "Primary" because, in a production environment, having more than one DC is recommended for redundancy. Feel free to choose any name you prefer.
    * **ISO Image:**
        ~ Select the Server 2019 ISO file that you previously downloaded.
    * Other fields will automatically be populated. Leave the “Skip unattended installation” box unchecked, then click “Next”.


2.  Choose the credential (username and password) that you will use to log on to the server after boot up. Remember to check the “Guest Additions” box.

<img src="https://cdn-images-1.medium.com/max/1200/1*8597DE4KuKSjs0kKFHP5Gg.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

3.  Allocate base memory and processor based on your host hardware resources (RAM and CPU). Remember to stay within the green area of the bar.

<img src="https://cdn-images-1.medium.com/max/1200/1*QaEhYoZFKjQva2db9QUbNA.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

4.  Select the “Create Virtual Hard Disk Now” and allocate the disk size. I decided to use 50 GB.

<img src="https://cdn-images-1.medium.com/max/1200/1*wLHqIcpICRrmwAH_fQSXSQ.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

5.  Check the summary to be sure everything is okay, then click “Finish.”

<img src="https://cdn-images-1.medium.com/max/1200/1*ZjLYK7NPtao720JnBfm6Uw.png" height="40%" width="80%" alt="screenshot of interface"/>
<br />

    It will take a while to load files and then display the screen below:

<img src="https://cdn-images-1.medium.com/max/1200/1*2umEZtunujMWPNLV8gKMVg.jpeg" height="40%" width="80%" alt="screenshot of interface"/>
<br />

6.  Click next and select one of the options with “Desktop Experience” to enable Graphical User Interface (GUI) on the server. Otherwise, it will just be command-line.

<img src="https://cdn-images-1.medium.com/max/1200/1*AN8Upttx1JDMC8zFkm8jnA.jpeg" height="30%" width="60%" alt="screenshot of interface"/>
<br />

7.  Click “Next” => accept license agreement => Next => Click “custom install”.

<img src="https://cdn-images-1.medium.com/max/1200/1*x6QdRiX3PRIzTd2zB0flNw.jpeg" height="30%" width="60%" alt="screenshot of interface"/>
<br />

8.  Click next, and the server will start to install. After a while, it will boot into Windows eventually.

9.  Set the credentials for the built-in administrator account.

<img src="https://cdn-images-1.medium.com/max/1200/1*Z6ImwRepbfv_GZVGaVlNSQ.jpeg" height="30%" width="60%" alt="screenshot of interface"/>
<br />

10. Once you click “Finish,” it will boot up into the Windows GUI. Select “Input” => “Keyboard” => “Insert Ctrl-Alt-Del” to display the administrator and password field.

<img src="https://cdn-images-1.medium.com/max/1200/1*Z865pDY-W0xZsKpLeN0cDg.png" height="30%" width="60%" alt="screenshot of interface"/>
<br />

**Your turn!** Follow the steps above to launch a virtual machine and the Windows 11 ISO you downloaded.

## Summary
So far, you have downloaded and installed VirtualBox, provisioned virtual machines, and installed operating systems. That is quite a lot you have accomplished already! In the next part, we will configure our Domain Controller and do a lot more fun stuff.
