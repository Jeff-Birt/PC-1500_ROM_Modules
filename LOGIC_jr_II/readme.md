# LOGIC jr II ROM module dump

LOGIC jr II is a HVAC related software package. It uses a 64K EPROM with a bank swtiching scheme to swap in 16K at a time into the 16K ROM address area. This process is described on this wepage: http://www.pc-1500.info/2015/03/16/edtech-inc-administrator-memory-module/ . While this LOGIC jr II module was glued together dumping the first/default bank was enough to recognize the bank swtitching scheme.

To dump the ROM the CE-158 RS232 interface was used. After configuring the CE-158 to redirect cassette operations to serial this command was used to dump the ROM contents: CSAVEM"LOGIC";&0000,&3FFF . To swtich from bank to bank I typed in 'POKE &5805,0', dumped this bank with the CE-158, then 'POKE &5806,0', dumped this bank with the CE-158 and so on.

LHtools was then used to convert the binary files to human readable form including BASIC program listings. See the file "Logic_Jr_II_Notes.txt" for more information.

Files
EDTECH_SCH.jpg                  - Image from PC-1500.org of bank swtiching cart schematic
Logic_jr_II.frag                - Framgment file used with LHtools to convert binary file to source
Logic_Jr_II_580A_Dump.txt       - '580A' bank of program convereted to text with LHtools
Logic_Jr_II_5805_Dump.txt       - '5805' bank of program convereted to text with LHtools
Logic_Jr_II_5806_Dump.txt       - '5806' bank of program convereted to text with LHtools
Logic_Jr_II_5808_Dump.txt       - '5809' bank of program convereted to text with LHtools
Logic_Jr_II_CE158_580A_Raw.bin  - '580A' bank of program raw dump from CE-158
Logic_Jr_II_CE158_5805_Raw.bin  - '5805' bank of program raw dump from CE-158
Logic_Jr_II_CE158_5806_Raw.bin  - '5806' bank of program raw dump from CE-158
Logic_Jr_II_CE158_5809_Raw.bin  - '5809' bank of program raw dump from CE-158
Logic_Jr_II_Dump.PNG            - Screen shot of terminal program with file being dumped 
Logic_Jr_II_Notes.txt           - Notes on file structure and LHtools command lines used
readme.md                       - this file

