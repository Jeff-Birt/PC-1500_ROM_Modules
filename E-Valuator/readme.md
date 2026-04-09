# Evaluator 

Dumped from two different versions of 60P program module. Each module contained three 4K EPROMs (12K) plus a 2K SRAM. More details in ROM folder.

The detoken15.js tool from the SBASIC VSCode extention was then used to detokenize the BASIC file *.ASC and save the Reserve memory out as *.RSV (first section of this is still the ML). 


Files

Images                          - Folder of product images
    Forced_Air                  - Folder for Forced Air module images
    Gas_Heating                 - Folder for Gas Heating module images
ROM                             - Folder containing ROM images and detokenized files
    Forced_Air                  - Folder for 30007 module files
        FAS.ASC                 - BASIC file in tewxt (ASCII)
        FAS.BIN                 - FAS_C1.BIN + FAS_C2.BIN + FAS_C3.BIN with ROM header overwritten
        FAS.RSV                 - Reserve memory binary file
        FAS_C1.BIN              - Dump of ROM C1
        FAS_C1_ML.BIN           - ML header section of FAS_C1.BIN extracted
        FAS_C1_ML_Header.TXT    - Dissasembly of ML with notes
        FAS_C1_ROMHDR.BIN       - FAS_C1.BIN with ROM header overwritten on bytes 0-7
        FAS_C2.BIN              - Dump of ROM C2
        FAS_C3.BIN              - Dump of ROM C3
        readme.md               - readme for this ROM
    Gas_Heating                 - Folder for Gas Heating module files
        GHR.ASC                 - BASIC file in tewxt (ASCII)
        GHR.BIN                 - GHR_C1.BIN + GHR_C2.BIN + GHR_C3.BIN with ROM header overwritten
        GHR.RSV                 - Reserve memory binary file
        GHR_C1.BIN              - Dump of ROM C1
        GHR_C1_ML_Header.BIN    - ML header section of GHR_C1.BIN extracted
        GHR_C1_ML_Header.TXT    - Dissasembly of ML with notes
        GHR_C1_ROMHDR.BIN       - GHR_C1.BIN with ROM header overwritten on bytes 0-7
        GHR_C2.BIN              - Dump of ROM C2
        GHR_C3.BIN              - Dump of ROM C3
        readme.md               - read me for this ROM
readme.md                       - this file

    
