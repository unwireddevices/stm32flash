# stm32flash

stm32flash (https://sourceforge.net/projects/stm32flash/) with some fixes, including:
* support for erasing more than 255 pages (for example, STM32L151CC has 1024 flash pages, and it doesn't support mass erase)
* support for writing/reading EEPROM on STM32L0 and STM32L1

To program flash memory on STM32L151CC:
stm32flash -b 230400 -e 1024 -w file.hex COMxx

To program EEPROM memory:
stm32flash -b 230400 -S 0x08080000 -w file.bin COMxx

P.S. Default UART baud rate is 115200 bps. Speeds up to 921600 bps were tested with CP2102 based USB-UART adapter. Even higher 3000000 bps speed should be possible with FT232R.
