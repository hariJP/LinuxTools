<p align="center"><b>LinuxTools</b></p>
<p align="center"><b>Here i've given commands to install essential linux tools that can save your time.</b></p>

##

### CLI's


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
  
  FOR SPEAKER ISSUES
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
    
    FOR CUSTOMIZATION
    
    to install tweaks for customization we need to add a repository by ``sudo add-apt-repository universe```
     then ```sudo apt install gnome-tweak-tool``` then search in applications search bar as "tweaks" to use tweaks.
     
    to install unity tweak tool "sudo apt install unity-tweak-tool" then search in applications search bar as "unitytweaks" to use unity-tweaks.
    
    - For apache2 server in linux 
    
    
      ```sudo apt update```
    then
      ```sudo apt install apache2```
    
    For reference
    
    https://ubuntu.com/tutorials/install-and-configure-apache#1-overview
    
    
    -For text editor
    
    ```sudo apt-get install -y mousepad```
    
    
    
    
    
    
    
    
    
    
    
    
  
