# EV3Locomotive
![Photo of train controller](Pictures\Photo1.jpg)

# Video
![video on youtube]()

# Features
* Operate locomotive by emulation of keystrokes on PC
* Works via Wi-Fi
* Support custom keystroke logic via .py module
* Show your own .bmp photos or text on display

# Installation
## On ev3
### 1. ev3dev
Install ev3dev on your ev3 by following [this instruction](https://www.ev3dev.org/docs/getting-started/)
### 2. Connect
Connect to your ev3 via SSH by following [this instruction](https://www.ev3dev.org/docs/tutorials/connecting-to-ev3dev-with-ssh/)
### 3. Cloning repo
Clone this repo by this command:
```
git clone https://github.com/Svinada/Ev3Locomotive.git
```
### 4. Run script
First of all run `PCdriver.exe` or `PC.py` on your PC. On ev3 open created folder by 
```
cd Ev3Locomotive
```
and run `TrainControllerV2.py` by 
```
python3 TrainControllerV2.py
```
Script will requre calibration, just follow its instruction. When calibration done, script will requre local IP of your PC and port which you entered in `PCdriver.exe` (it contains in `config.ini`). By the way script does not remember entered IP and port and will ask it everytime, but you can open script by 
```
nano TrainControllerV2.py
```
and change line (14 and 15) with your ip and port:
```
...
import select
import json

ip = "" <-- Change this, ip should be string
port = 0 <-- And this, port should be number

thrust = 0
thrust_maximum = 0
...
```
Then press `CTRL+X`, save modified buffer by `Y` and press `Enter`.
### 5. Selecting different locomotives or game profiles
`Left` and `right` buttons on ev3 will change current locomotive, but if at first you press `up` button, you are able to change game profiles (press button `up` again to load current profile and select locomotives).
### 6. Exit
Stop script by pressing `backspace` button on ev3 or press `CTRL+C` in SSH window.
## On PC
### With default configs
Just download latest release with name `PCdriver_and_default_configs.zip` [from here](https://github.com/Svinada/Ev3Locomotive/releases) (default port is `9600`, you can change it in `config.ini`).
### Without default configs
Download `PCdriver.exe` [from here](https://github.com/Svinada/Ev3Locomotive/releases).
