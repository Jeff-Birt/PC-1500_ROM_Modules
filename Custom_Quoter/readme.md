# Custom Quoter

Dumped from two different versions of 60P program module. Each module contained two EPROMs which were read and then combined into a single binary file and detokenized.Thus the combined BIN file contains the ROM header but not the CE-158 header. 

PROG_30007_A.BIN & PROG_30007_B.BIN ->> PROG_30007_AB.BIN ->> PROG_30007_AB.TXT

LHtools was then used to convert the binary files to human readable form including BASIC program listings. 


Files

Images                          - Folder of product images
    30007                       - Folder for 30007 module images
    30025                       - Folder for 30025 module images
Manual                          - Manual folder
    KB_Overlay.PNG              - Keyboard Overlay
    Model_300_Ref_Card_F.PNG    - Model 300 Reference Card Front
    Model_300_Ref_Card_R.PNG    - Model 300 Reference Card Rear
ROM                             - Folder containing ROM images and detokenized files
    30007                       - Folder for 30007 module files
        PROG_30007_A.BIN        - Dump of A EPROM
        PROG_30007_AB.bin       - Combined A&B EPROMs
        PROG_30007_AB.txt       - Text file (ASCII) of BASIC program
        PROG_30007_AB_BAS.bin   - Binary of BASIC program memory with no header
        PROG_30007_AB_DAT.bin   - Machine code or data, used by BASIC program
        PROG_30007_AB_RES.bin   - Binary of Reserve memory with no header
        PROG_30007_B.BIN        - Dump of A EPROM
    30025                       - Folder for 30025 module files
        PROG_30025_A.BIN        - Dump of A EPROM
        PROG_30025_AB.bin       - Combined A&B EPROMs
        PROG_30025_AB.txt       - Text file (ASCII) of BASIC program
        PROG_30025_AB_BAS.bin   - Binary of BASIC program memory with no header
        PROG_30025_AB_DAT.bin   - Machine code or data, used by BASIC program
        PROG_30025_AB_RES.bin   - Binary of Reserve memory with no header
        PROG_30025_B.BIN        - Dump of A EPROM
    CusQuote.frag               - Fragment file for use with with LHtools
    Dump_Notes.txt              - Note of dumping of this particular ROM
readme.md                       - this file

    
