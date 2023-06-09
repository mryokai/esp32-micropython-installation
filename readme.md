Read https://docs.micropython.org/en/latest/esp32/tutorial/intro.html  
Install micropython on ESP32 board https://micropython.org/download/esp32/  
  &ensp;Use esptools.py method from the tutorial. Or  
  &ensp;Use Flash Download Tool from espressif https://www.espressif.com/en/support/download/other-tools  
  &ensp;![image](https://github.com/mryokai/esp32-micropython-installation/assets/136013177/eeda586c-f026-47a2-a0fb-729715f728be)  
Create python vitrual environment and activate  
pip install esptool  
esptool.py --port COM13 erase_flash  
esptool.py --chip esp32 --port COM13 write_flash -z 0x1000 esp32-20180511-v1.9.4.bin  
pip3 install rshell  

Ubuntu:  
Create python vitrual environment and activate   
pip3 install rshell
sudo usermod -a -G dialout $USER
rshell -h



