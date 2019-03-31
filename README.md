# Shutdown Switch Raspberry Pi

Simple script python3 to shutdown Raspberry pi to external button

### Requirements

#### Hardware

* Raspberry Pi
* Resistor 10K
* Button NO

#### Software

* raspbian
* Python 3 and PIP

### Prerequisite

Connect resistor between 3.3V (pin 1) and pin select in script. The button is connected between pin select in script and any GND pin. 

### Installation
* Download from Github, install pip3 and add permissions.
    ```sh
    $ git clone https://github.com/GuillermoElectrico/power-switch-Pi
	$ sudo apt-get install python3-pip
	$ sudo pip3 install --upgrade RPi.GPIO
	$ cd power-switch-Pi/
	$ sudo chmod+x power-switch-Pi.py
    ```
* Edit script and modify InputPin as unused pin in the board

* To run the python script at system startup. Add to following lines to the end of /etc/rc.local but before exit:
    ```sh
    # Start Power Switch Raspberry Pi
    /home/--user--/power-switch-Pi/power-switch-Pi.py > /var/log/power_swich.log &
    ```
