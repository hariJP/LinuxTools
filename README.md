<p align="center"><b>LinuxTools</b></p>
<p align="center"><b>Here i've given commands to install essential linux tools that can save your time.</dev/sda1/b></p>

##

### CLI's

- For Formatting a Pendrive(Fat32)
  ```lsblk```
  ```sudo umount /dev/sdb```
   ```sudo mkfs.fat -F 32 /dev/sdb```
   here ***/dev/sdb*** can be replaced by your respective storage device revealed by lsblk list
   
- For Adjusting Screen Brightness
  ```xrandr --output LVDS-1 --brightness 0.8```
   here ***LVDS-1*** can be replaced by your respective output device

- For Adjusting Audio
  ```sudo apt-get install alsa-utils```
  and then
  ```alsamixer```

- For Adjusting Date & Time
  ```sudo date -s"01 OCT 2022 09:15:00 AM" ```
##

### GUI's

- For Multimedia accessibility
  ```sudo apt-get install vlc```

- For updating your firefox 
  ```sudo apt-get install firefox-esr```

- For screen recording services
  ```sudo apt-get install simplescreenrecorder```

- For docs
  ```sudo apt-get install libreoffice```
  
  ##
  
  
  ### ADDITIONAL CUSTOMIZATIONS FOR SIMPLE AND CONVENIENT INTERFACING WITH YOUR LINUX
  
  ```FOR SPEAKER ISSUES```
  - 
    Open the terminal (keyboard shortcut Ctrl+Alt+T).
    Copy/paste "sudo gedit /usr/share/pulseaudio/alsa-mixer/paths/analog-output-speaker.conf" and press Enter.
    When prompted, type your password and press Enter.
    A text file called analog-output-speaker.conf will open up in a new window. In the text file, find this part:

    [Element Headphone]
    switch = off
    volume = off
    	

    and change it to this:

    [Element Headphone]
    switch = off
    volume = merge
    override-map.1 = all
    override-map.2 = all-left,all-right
    	

    Next, in the same text file, find this part:

    [Element Speaker]
    required-any = any
    switch = mute
    volume = merge
    override-map.1 = all
    override-map.2 = all-left,all-right
    	

    and change it to this:

    [Element Speaker]
    required-any = any
    switch = mute
    volume = off
    	

    Save your changes to analog-output-speaker.conf using either Ctrl+S or the save button at the top of the file editor.
    Go back to the terminal, type sudo reboot and press Enter to reset your Toughbook.
    Once your Toughbook boots back up, check the audio. It should be working now.```
    
    ##
    
    ###
    
    ```-FOR CUSTOMIZATION```
    
    -to install tweaks for customization we need to add a repository by 
    
    ```sudo add-apt-repository universe```
     then
     
     ```sudo apt install gnome-tweak-tool``` 
     /dev/sda1
     then search in applications search bar as ```tweaks``` to use tweaks.
     
    -to install unity tweak tool 
    ```sudo apt install unity-tweak-tool``` 
    
    then search in applications search bar as ```unitytweaks``` to use unity-tweaks.

##
    For apache2 server in linux 
    
    
      ```sudo apt update```
    
    then
      
      ```sudo apt install apache2```
    
    For reference
    
    ```https://ubuntu.com/tutorials/install-and-configure-apache#1-overview```/dev/sda1
    
##    
    To install visual studio code for 32-bit ubuntu(debian)
       
       ```wget https://drive.google.com/file/d/1UHQNNBq5jazdpHydTUMFUCTjfIbT65DF/view?usp=sharing```
##       
     To install arduino IDE for 32-bit ubuntu(debian)
       
       ```wget https://drive.google.com/file/d/1xC1dLXHOV-f24OnDAnIty6SY23YwOOUp/view?usp=sharing```
      
    
##    
    -For installing mousepad text editor
    
    ```sudo apt-get install -y mousepad```
##    
    -For document viewing
    
     ```sudo apt-get install atril```
     
##

######
    
    ### TO CREATE A BOOTABLE USB DRIVE USING LINUX TERMINAL
    
    -For creating a bootable USB drive using linux terminal you have to insert your fresh USB pendrive then make sure it is formatted in a FAT32 format
    then we have to backup the contents of the PC which you are going to install the new Operating Sytem(OS) make sure you are backed up all the contents 
    and after inserted the pendrive in the USB port we have to find the disk address allotted the pendrive port to find that type ```sudo fdisk -l```
    enter the linux password and the output will display the all storage devices associated with you device find out the pendrive address in my case
    it is ```/dev/sda1```
    
    -After finding out the pendrive's address we have to find the path of the iso file and its name with correct representation as it is stored
    in our computer in my case i've kept the .iso file in my Downloads folder like this ```/home/kali/Downloads/ubuntu_i386.iso``` 
    
    -Now open the terminal and type line in these format 
    ```$ sudo dd if=/[ISOFILE-LOCATION] of=/dev/[PARTITION NAME] status=progress offlag=sync```
    
    i have replaced the .iso file location by my file location in ```if=/home/kali/Downloads/ubuntu_i386.iso```
    and the iso file should be kept in the targetted disk that is my pendrive address that we found earlier ``` /dev/sda1```
    
    hence the line becomes ```$ sudo dd if=/home/kali/Downloads/ubuntu_i386.iso of=/dev/sda1 status=progress offlag=sync``` in my case.
    
    wait until the terminal completely writes the iso file in bootable pendrive the after comletion properly exit the terminal to avoid corruption
    in the bootable pendrive.
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
    
  
