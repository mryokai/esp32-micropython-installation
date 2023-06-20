Read https://docs.micropython.org/en/latest/esp32/tutorial/intro.html  
Install micropython on ESP32 board  
  &ensp;Download binary from https://micropython.org/download/esp32/  
  &ensp;Method 1: Flash Download Tool with Windows  
  &ensp;&ensp;Use Flash Download Tool from espressif https://www.espressif.com/en/support/download/other-tools  
  &ensp;&ensp;![image](https://github.com/mryokai/esp32-micropython-installation/assets/136013177/eeda586c-f026-47a2-a0fb-729715f728be)  
  &ensp;Method 2: Use esptools.py method from the tutorial  
  &ensp;&ensp;Create python vitrual environment and activate  
  &ensp;&ensp;pip install esptool  
  &ensp;&ensp;Open Device Manager to find COM port # by pluging in and out the ESP32 board.  
  &ensp;&ensp;esptool.py --port COM13 erase_flash  
  &ensp;&ensp;esptool.py --chip esp32 --port COM6 write_flash -z 0x1000 esp32-20180511-v1.9.4.bin  
  
* rshell does not run in Win10!!!  
For developement using Win10:  
  &ensp;&ensp;Go to the python virtual environment  
  &ensp;&ensp;pip install mpfshell  
  &ensp;&ensp;mpfshell -c "open COM6"  
  &ensp;&ensp;help
  &ensp;&ensp;exit
  &ensp;&ensp;Install and open vscode
  &ensp;&ensp;Write python code in main.py and use mpfshell to put main.py (and any necessary libraries) to the ESP32 board.

  
For developement using Ubuntu:  
  &ensp;Install python3-tk if not already installed  
  &ensp;&ensp;sudo apt install python3-tk  
  &ensp;Create python vitrual environment and activate   
  &ensp;pip3 install rshell  
  &ensp;sudo usermod -a -G dialout $USER  
  &ensp;rshell -h  
  &ensp;exit rshell  
  &ensp;pip3 install thonny  
  &ensp;run thonny within venv  
  &ensp;Tools->Options->Interpreter ---> MicroPython(ESP32) and Port -> OK  
  &ensp;Write program  
  &ensp;Save as main.py (to device)  
  &ensp;Save other libraries (to device)  
  &ensp;Press reset (hard reset) on device, main.py will run  
  
  
Reference1: https://github.com/dhylands/rshell  


