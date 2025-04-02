# AWSButton
a single button that logs to the TPZ server

This is designed to run on a Raspberry Zero. The single button is on pin 2 and connected to ground
The bashrc file has been modified on the Rpi image to start the python code at boot. This grabs and holds the terminal, which is regretable.
to set this up, use  "Method 2: .bashrc" from this website: https://www.dexterindustries.com/howto/run-a-program-on-your-raspberry-pi-at-startup/

Method 2: .bashrc


The second method to run a program on your Raspberry Pi at startup is to modify the .bashrc  file. With the .bashrc method, your python program will run when you log in (which happens automatically when you boot up and go directly to the desktop) and also every time when a new terminal is opened, or when a new SSH connection is made. Put your command at the bottom of ‘/home/pi/.bashrc’. The program can be aborted with ‘ctrl-c’ while it is running!

**sudo nano /home/pi/.bashrc**
Go to the last line of the script and add:

**echo Running at boot 
sudo python /home/pi/awsCallPlusButton2.py**
The echo statement above is used to show that the commands in .bashrc file are executed on bootup as well as connecting to bash console.

Bash RC Configure systemd Run a Program On Your Raspberry Pi At Startup

Now reboot the Pi to hear the Pi speak at startup.

**sudo reboot**
