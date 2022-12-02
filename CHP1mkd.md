# Chapter 1: Set up labs.

### Download links



[Virtual Box](https://www.virtualbox.org/wiki/Downloads)



[Metasploitable](https://sourceforge.net/projects/metasploitable/)

[Kali Linux](https://kali.org/get-kali/#kali-virtual-machines)

[Ubuntu](https://ubuntu.com/)



### Setting up the VM's

#### VirtualBox

Before we begin to set up the virtual machines, your virtual sandbox, we need to download and install VirtualBox. This will be the main program that will store, and run, all of our virtual computers. A Quote from chapter one `Think of VirtualBox as a program that lets you build virtual computers.`

We can download VirtualBox from [here](https://www.virtualbox.org/wiki/Downloads). Once we have it downloaded and installed we can begin to build the virtual computers we will be using in the lab.

#### 7zip (Windows)

If you have 7zip, you can bypass this step. A few of the images we are going download here will not properly extract with the base tools on a Windows PC. Travel to the [7zip](https://7zip.org/download.html) page and select the 64-bit Windows x64 executable. This will ensure we can properly extract some of the Operating System images we will be downloading.

#### PfSense

PfSense acts as a router and a firewall for the virtual machines we will be using. Since we are going to be using machines that are vulnerable by design, and running active attacks, we are going to need a bit more security. Travel to the [PfSense](https://www.pfsense.org/download/) download page, slect the amd64 Architecture, and then the DVD Image (ISO) Installer. Click the Download button, and we have our first iso almost ready. With PfSense, we need to enter into our Downloads folder and right click. 