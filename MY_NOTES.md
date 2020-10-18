https://github.com/arendst/Tasmota/wiki/Esptool

adapter pinout:
https://hackster.imgix.net/uploads/attachments/455086/bootloading1_E4979vb4St.JPG?auto=compress%2Cformat&w=1280&h=960&fit=max

install esptool:
python get-pip.py
python -m pip install esptool

backup device:
python -m esptool.py --port COM8 read_flash 0x00000 0x100000 leering_image1M.bin
/c/Python27/python -m esptool --port COM8 read_flash 0x00000 0x100000 sohoffR3_image1M.bin

erase firmware:
python -m esptool.py --port COM8 erase_flash
/c/Python27/python -m esptool --port COM8 erase_flash
