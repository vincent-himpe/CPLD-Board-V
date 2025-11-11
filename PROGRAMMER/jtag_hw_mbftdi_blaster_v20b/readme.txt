Copy the jtag_hw_mbftdi_blaster64.dll file to the Quartus folder, for example, d:\altera\18.1\quartus\bin64\, if you have 64-bit Windows and, accordingly, the 64-bit version of Quartus 18.1 installed.

If you have 32-bit Windows, then copy jtag_hw_mbftdi_blaster32.dll to the Quartus folder d:\altera\13.0\quartus\bin\
(or whatever version you have installed).

If the file already exists (a previous version is installed) and is write-protected, you need to stop the jtagserver.exe process in the task manager and then copy it.

Version 2.0b of the jtag_hw_mbftdi_blaster64 programmer can use the mbftdi.cfg configuration text file. It should be located next to the DLL file, in the same folder.
It can contain two parameters:
channel=1
and frequency=2500000

Channel determines which mpsse channel will be used. For channel A, channel=0; for channel B, channel=1.
The second parameter, frequency, determines the JTAG clock rate (default: 10 MHz).


---------------- MORE INFORMATION -------------------------

https://marsohod.org/378-mbftdi-jtag-channel-b


----------------- ORIGINAL README : -----------------------



Скопируйте файл jtag_hw_mbftdi_blaster64.dll в папку квартуса, например, d:\altera\18.1\quartus\bin64\, если у вас установлена 64х битная Windows и соответственно 64х битная версия Quartus 18.1.

Если у вас 32-х битный windows, то копируйте jtag_hw_mbftdi_blaster32.dll в папку квартуса d:\altera\13.0\quartus\bin\
(ну или какая версия у вас установлена).

Если файл уже существует (предыдущая версия установлена) и оказывается защищенным от записи, то нужно остановить процесс jtagserver.exe в диспетчере задач.

----------------------------------
v2.0b
Версия 2.0b программатора jtag_hw_mbftdi_blaster64 может использовать конфигурационный текстовый файл mbftdi.cfg.
В нем может содержаться два параметра:
channel=1
frequency=2500000

channel определяет какой из каналов mpsse будет использоваться. Для канала A channel=0, для канала B channel=1.
Второй параметр frequency определяет тактовую тастоту на JTAG (по умолчанию 10МГц).

----------------------------------
v1.8b
Добавлена поддержка микросхем FT4232.
Повышена скорость работы в режиме ActiveSerial.
Улучшена внутренняя структура кода.

----------------------------------
v1.6b
теперь можно загружать FPGA Cyclone V.

----------------------------------
v1.4b
Исправлены баги работы программатора с Quartus II v12.1 в 64-х битной WIndows 7.
Изменено название драйвера (чтобы облегчить определение его типа). Теперь название DLL включает в себя собственно тип используемой платформы.



