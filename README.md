# Robot claw

Code for controlling a 3 axis robot arm + claw with a PS4 controller. _Disclamer: this code has been written in about an hour and was never meant to be shared._

## Hardware
* RPi zero
* Servo Driver HAT for Raspberry Pi
* HD-1900A servo * 4
* PS4 Controller
* Robo arm

## Installation

1. Turn on SPI via `sudo raspi-config`
    ```
    Interfacing Options -> I2C
   ```
2. Install dependencies
    ```
    sudo apt update
    sudo apt-get install python3-pip 
    pip3 install pyPS4Controller
   
## Connect PS4 controller to RPi
1. Start scanning for bluetooth devices
```
sudo bluetoothctl
agent on
default-agent
scan on
```
2. Hold Options and the PS button on your controller
```
connect MAC_ADDRESS_OF_YOUR_CONTROLLER
trust MAC_ADDRESS_OF_YOUR_CONTROLLER
quit
```
