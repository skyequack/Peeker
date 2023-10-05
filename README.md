# Peeker
Small Surveillance Bot

## Introduction:
Peeker is a small mobile robot with a continuous track drive with surveillance and scouting capabilities which is light enough to be carried around easily and rugged enough to survive throws and drops. Equipped with a camera, a microphone, and sensors such as an infrared sharp sensor and hazardous gas sensor, the bot is able to gather intelligence from otherwise inaccessible areas. The processing power and wireless capabilities of a Raspberry Pi 4 allow Peeker to be controlled remotely while also being capable of live-streaming audio and video to the user via WiFi. Moreover, Peeker features a novel 'flipping mechanism' that, as the name implies, allows the bot to correct itself in the event of flipping over. 

## Proposed Design:
### Robot:
The bot is low profile with a foladable camera mount with 3 degrees of freedom. The drive used is a continuous track drive with two rollers. While in the 'inactive' state, the camera mount folds flat and hence is able to avoid getting damaged when tossed. The design of the mount also enables it to act as the mentioned flipping mechanism, helping the robot regain funtionality in the event of being turned upside down. The mount also features an antenna to assist in wireless communication with the controller.

### Controller:
The controller is custom made and hosts a Raspberry Pi 0 w and has an LCD display which can output the video feed from the robot. 

## Electronics:
The control unit decided for this bot is the Raspeberry Pi 4 due it its video processesing capabilites, as well as built in support for wireless communication. The GPIO pins on the board are sufficient to connect all required parts without the need for expansion boards. The driver motors proposed are 12V 500RPM DC motors with a threaded shaft for ease of coupling. The motor driver board selected is the Pololu MAX14870 as it has a very small form factor is holds a lot of advantages such as
