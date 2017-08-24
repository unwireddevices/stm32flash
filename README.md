# stm32flash

stm32flash (https://sourceforge.net/projects/stm32flash/) with some fixes, including:
* support for erasing more than 255 pages (STM32L151CC has 1024 flash pages, and it doesn't support mass erase)
* support for writing/reading EEPROM on STM32L0 and STM32L1
