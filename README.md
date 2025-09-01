# How to install Ubuntu on mac

I'll show how to install a VirtualMachine with Linux Ubuntu on it on your Mac. We are going to use UTM to create the VirtualMachine. This guide won't be a technical one, but for some informatics could be a little be naif; I will be very essential and I will explain just the basics to install Ubuntu on your M1/M2/M3/M4 Mac. If you have a Intel Mac you can find some usefull guide online to install a Linux Virtual Machine with your processor. <br>

First of all some basics information and terms that I'm going to use:
- VM : Virtual Machine.
- OS : Operating System.
- Linux image : we refer to an image of a Operating System when we talk about a file which contains all the information necessary to download and use a OS.
There are several option to create and use a VM on your Mac, but I choose to use UTM, which is easy to use, and most important thing, free to use. I also choose to install Ubuntu and no other version of Linux, just for personal preference. <br>

In this guide I'll show you some image from a pc to guide you easily, all the photos are taken from **Datastream** youtube [video](https://www.youtube.com/watch?v=1PL-0-5BNXs), which explain very well how to install Ubuntu on your Mac. I'll follow the same process of that video.


## Contents
- [Install Ubuntu](#Install-Ubuntu)
- [Install UTM and create the Virtual Machine](#Install-UTM-and-create-the-Virtual-Machine)
- [Configure the Virtual Machine](#Configure-the-Virtual-Machine)
- [Finish to set-up](#Finish-to-set-up)


### Install Ubuntu

As you can imagine to have a Linux computer we have to install Linux on our pc. So, the first thing we have to do is download the Ubuntu image. You have to go to the official [Ubuntu website](https://ubuntu.com/), select *product*, then *Ubuntu server* (we need the server versione because it is the only possibility with an ARM processor), click on *Alternative architectures*, select *ARM* and click on the green download bottom. Once you have done this you will have on your Mac a file like:
```
ubuntu-24.04.3-live-server-arm64 16.47.29.iso
```

![ubuntu1](/image/ubuntu1.png)
![ubuntu2](/image/ubuntu2.png)
![ubuntu3](/image/ubuntu3.png)
![ubuntu4](/image/ubuntu4.png)

### Install UTM and create the Virtual Machine

Install UTM is an easy step. You have just to go to [UTM website](https://mac.getutm.app/) and download the program. Once you have done you can create a VM. Select *Virtualize*, then *Linux* with in *Boot ISO image* your .iso file that you have downloaded from Ubuntu website. Now you have to choose how much memory dedicate to your VM, if you don't know how much space use just leave the default settings. It is suggested *Enable hardware OpenGL acceleration* to improve some graphics aspects. To finish just save the Virtual Machine.

![VM1](/image/VM1.png)
![VM2](/image/VM2.png)
![VM3](/image/VM3.png)


### Configure the Virtual Machine

Now the most difficult part of the guide, but don't worry. Launch the VM from UTM and select *Try or install Ubuntu Server* to start the installation process. Now you can complete the installation process as you prefer, but if you want I can show how I did. Just kepp in mind to configure properly your keyboard and username and password.

![installation1](/image/installation1.png)
![installation2](/image/installation2.png)
![installation3](/image/installation3.png)
![installation4](/image/installation4.png)
![installation5](/image/installation5.png)
![installation6](/image/installation6.png)
![installation7](/image/installation7.png)
![installation8](/image/installation8.png)
![installation9](/image/installation9.png)
![installation10](/image/installation10.png)
![installation11](/image/installation11.png)

Once the installation process is completed will be on the screen the option *Reboot now*, press *enter* and then close the VM. At this point we have to remove the image of Linux from our VM to avoid that the installation process starts all over again. Select your VM, go to *CD/DVD* and select *clear*.

![installation12](/image/installation12.png)

Now you can start your VM and log-in in the terminal interface that will show to you. Once you have done you have to write:
```
sudo apt update
```
to update all the packages. You have to write also:
```
sudo apt install ubuntu-desktop
```
to install Ubuntu desktop and have a graphics interface. To complete write:
```
sudo reboot now
```
to restart the VM. Once the log-in screen will be on the screen just write your password and finish the installation.


### Finish to set-up

The last two step before use our new Linux VM is complete the configuration settings and install drivers. To do that open the terminal and write:
```
sudo apt intall spice-vdagent spice-webdavd
```
after they are installed power off the VM. In UTM settings for your VM select *sharing*, from *Directory share Mode* select *SPICE WebDAV* and a folder that you want to share between VM and Mac (in *Path*). Also if you go on *Display* VM settings and enable *Retina Mode* you can improve the graphics for retina display.

![setup1](/image/setup1.png)
![setup2](/image/setup2.png)
![setup3](/image/setup3.png)
![setup4](/image/setup4.png)
