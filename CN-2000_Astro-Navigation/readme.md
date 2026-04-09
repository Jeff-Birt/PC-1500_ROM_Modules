# CN-2000 Astro-Navigation ROM

To dump the ROM EPROM was removed from the 60P module and read directly. Thus the BIN file contains the ROM header but not the CE-158 header. 

The 'detokenize15.js' program included with the SBAS VSCode extension was used to convert the binary file to human readable form including BASIC program listings. 

Files

Images                              - Folder od images of module
ROM
    Astro_Nav.txt                   - Text file (ASCII) of BASIC program
    AstroNav.BIN                    - Dump of ROM
    Dump_Notes.txt                  - Note of dumping of this particular ROM
    readme.md                       - this file
Manual
    CN-2000_Astro-Navigation.pdf    - Manual scanned and OCRd
    
