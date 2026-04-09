# Prudential_Insurance_16K from Sharp xxx cart

To dump the ROM the CE-158 RS232 interface was used. After configuring the CE-158 to redirect cassette operations to serial this command was used to dump the ROM contents: CSAVEM"LOGIC";&0000,&3FFF . 

The 'detokenize15.js' program included with the SBAS VSCode extension was used to convert the binary file to human readable form including BASIC program listings. 

Files

Images

Prudential_16K.asc              - Text file (ASCII) of BASIC program
Prudential_16K.bin              - Dump of ROM with CE-158 header
readme.md                       - this file
    
