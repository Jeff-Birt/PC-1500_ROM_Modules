# CE-502B Statistics ROM from Sharp

To dump the ROM the CE-158 RS232 interface was used. After configuring the CE-158 to redirect cassette operations to serial this command was used to dump the ROM contents: CSAVEM"LOGIC";&0000,&3FFF . 

LHtools was then used to convert the binary files to human readable form including BASIC program listings. 

Files
CE-502B.BAS                     - Tokenized BASIC with CE-158 header
CE-502B.bin                     - Dump of RAM cart with CE-158 header, includes Reserve memory
CE-502B.frag                    - Fragment file for use with with LHtools
CE-502B.pc1500.sbs              - Text file (ASCII) of BASIC program 
CE-502B.RSV                     - Reserve memory with CE-158 header
readme.md                       - this file

