# Pygmy Software ROM module dump

There was no identifying information on this PC-1500 ROM module. It is some sort fo HVAC calcualtion program from the looks of it. While it uses a 16K EPROM it is wired up as an 8K module. To dump the ROM the CE-158 RS232 interface was used. After configuring the CE-158 to redirect cassette operations to serial this command was used to dump the ROM contents: CSAVEM"Pygmy";&0000,&3FFF

After discovering it was wired as an 8K module a hex editor was used to remove the CE-158 header and the first 8K of 0x00 filler. LHTools was then used to convert the binary file to a human readable form complete with BASIC listing. See file: Pygmy_Software_Unknown_Notes.txt for conversion notes.

I have not figured out what the correct entry point is to run this program. Typing 'RUN' will start at line 4 and you get an error for having a unmatched RETURN. There are several line labels used in the program so perhaps something like RUN "P" should be used?

Files
PC-1500_Pygmy_ROM_Dump.PNG              - Screen shot of termianl program with file being dumped
Pygmy.frag                              - Framgment file used with LHtools to convert binary file to source
Pygmy_Software_Unknown_8K_RAW.bin       - Dumped file with CE-158 header and lower blank 8K removed
Pygmy_Software_Unknown_CE158_RAW.bin    - Raw dump from CE-158 as a 16K cart, was really an 8K cart
Pygmy_Software_Unknown_Dump.txt         - Program convereted to text with LHtools
Pygmy_Software_Unknown_Notes.txt        - Notes on how dump/conversion were done
readme.md                               - This file