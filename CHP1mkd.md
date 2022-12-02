# Chapter 1: Set up labs.

### Download links

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

PfSense acts as a router and a firewall for the virtual machines we will be using. Since we are going to be using machines that are vulnerable by design, and running active attacks, we are going to need a bit more security. Travel to the [PfSense](https://www.pfsense.org/download/) download page, slect the amd64 Architecture, and then the DVD Image (ISO) Installer. Click the Download button, and we have our first iso almost ready. With PfSense, we need to utilize the **7zip** program to extract the .vmdk file.

Once the file is extracted, we will begin to create our PfSense machine. To do so, click the **New** button. On the screen that pops up, we can name the machine. PfSense should be fine. If you have a preference on where you want the virtual machine saved, you can do so by changing the folder. In the ISO drop down, we are going to select the .iso file that we extracted from the zipped file. In the _Type_ drop down, we want to select **BSD**, followed by **FreeBSD (64-bit)** for the _Version_, and click Next.

On this page, titled **_Hardware_**, we can leave the _Base Memory_ at 1024 MB. We do, however want to change the processors for this machine to **2** (two). Once we have this set up, we can click next to the **_Virtual Hard Disk_**. No changes are necessary here, so we can click next once more. Click finish.

One last thing we have to change are the network settings for PfSense. Click the **Settings** button at the top of the machine details. In the left hand pane, we will select the **_Network_** tab. Here the **Adapter 1** can be left for a moment. We want to select the **Adapter 2** tab and click the box for _Enable Network Adapter_. Select _Internal Netwrok_ from the **Attached to:** drop down, and give it the name **_Internal LAN_**. Click the okay button, and we can run the machine.

If there is no internet for the PfSense, shutdown the machine. Open the settings back up, and change **Adapter 1** from **_NAT_** to **_Bridged_**.