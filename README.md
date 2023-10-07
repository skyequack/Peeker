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

### Control:
The control unit decided for this project is the Raspeberry Pi 4 due it its video processing capabilites, as well as built in support for wireless communication. The GPIO pins on the board are sufficient to connect all required parts without the need for expansion boards. 

### Drive:
The driver motors proposed are 12V 500RPM DC motors, with a max load current being 300 mA. The shaft is threaded for ease of coupling. The motor driver board selected is the Pololu TB6612FNG as it has a very small form factor and also holds a lot of advantages such as reverse polarity protection. The rated continuous output current is 1A which makes it more than sufficent for the selected DC motors. The Pololu TB6612FNG features two channels hence only one board is required to drive both the DC motors.

### Camera Mount:
The camera mount is similar to a robotic arm with a VRR configuration. This provides the camera (end effector) with three degrees of freedom. The camera can move laterally up and down, and has pitch and yaw. Each joint is actuated by a MG995 Metal Gear Servo Motor as it can provide stall torque of 11 KGcm and 6.6v which is more than the max required stall torque of 8 KGcm. The camera module used is AR1820HS due to its high resolution (18MP). The camera mount also doubles as a flipping mechanism by actuating the first R joint. The wireless antenna is mounted at 

### Sensors
The bot features a harmful gas sensor 'MQ-135' suitable for detecting NH3, NOx, alcohol, Benzene, smoke, CO2, etc. A microphone module relays audio data to the user. An inertial measurement unit IMU 6050 is used to sense orientational and positional data.

### Controller
The controller hosts a Raspberry Pi 0 w which receives all the data from the Raspberry Pi 4. Push buttons are used for user input and an LCD screen connected to the RPi 0w is used for displaying visual data, and a speaker module outputs audio data.
