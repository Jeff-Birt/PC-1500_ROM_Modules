# Pygmy Software Rheem_Heat_Master ROM

There was no identifying information on this PC-1500 ROM module. It is some sort fo HVAC calcualtion program from the looks of it. While it uses a 16K EPROM it is wired up as an 8K module. To dump the ROM the CE-158 RS232 interface was used. After configuring the CE-158 to redirect cassette operations to serial this command was used to dump the ROM contents: CSAVEM"Pygmy";&0000,&3FFF

After discovering it was wired as an 8K module a hex editor was used to remove the CE-158 header and the first 8K of 0x00 filler. LHTools was then used to convert the binary file to a human readable form complete with BASIC listing. See file: Pygmy_Software_Unknown_Notes.txt for conversion notes. Months later I detokenized and seperated the Reserve memory Binary with detokenize15.js from VSCode SBASIC extension.

I have not figured out what the correct entry point is to run this program. Typing 'RUN' will start at line 4 and you get an error for having a unmatched RETURN. There are several line labels used in the program so perhaps something like RUN "P" should be used?

Files
Pygmy.frag                                      - Framgment file used with LHtools to convert binary file to source
Pygmy_Software_Rheem_Heat_Master_Notes.txt      - Notes specfic to this ROM
Pygmy_Software_Rheem_Heat_Master.RSV            - Reserve memory binary file
Pygmy_Software_Rheem_Heat_Master_8K.ASC         - BASIC text file (ASCII) with CR line endings
Pygmy_Software_Rheem_Heat_Master_8K.bin         - Dumped file with CE-158 header and lower blank 8K removed
Pygmy_Software_Rheem_Heat_Master_CE158_RAW.bin  - Raw dump from CE-158 (with CE-158 header) as a 16K cart, was really an 8K cart
readme.md                                       - This file