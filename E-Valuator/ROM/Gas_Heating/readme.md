# Evaluator Forced Air ROM

This 60P ROM module containing 3 4K ROMs (12K) and also contains 2K of SRAM. There is no ROM header, rather there is ML from $0000~$0040 which is an initializtion routine that must be called before the program can be used. The 2K of SRAM seems to be mapped to $4800.

From $0041~$00C4 appears to be a Reserve memory area with BASIC starting at the normal $00C5 location in ROM.

The ML code from $0000~$0040 was extracted to GHR_C1_ML_Header.bin and disassbmled into GHR_C1_ML_Header.txt. A traditional ROM header was overwrittne on first 8 bytes of GHR_C1.BIN to create GHR_C1_ROMHDR.BIN and this file was concatenated with GHR_C2.BIN and GHR_C2.BIN to produce the complete binary as GHR.BIN.

The detoken15.js tool from the SBASIC VSCode extention was then used to detokenize the BASIC file GHR.ASC and save the Reserve memory out as GHR.RSV (first section of this is still the ML).

Files
GHR.ASC                     - BASIC file in tewxt (ASCII)
GHR.BIN                     - GHR_C1.BIN + GHR_C2.BIN + GHR_C3.BIN with ROM header overwritten
GHR.RSV                     - Reserve memory binary file
GHR_C1.BIN                  - Dump of ROM C1
GHR_C1_ML_Header.BIN        - ML header section of GHR_C1.BIN extracted
GHR_C1_ML_Header.TXT        - Dissasembly of ML with notes
GHR_C1_ROMHDR.BIN           - GHR_C1.BIN with ROM header overwritten on bytes 0-7
GHR_C2.BIN                  - Dump of ROM C2
GHR_C3.BIN                  - Dump of ROM C3
readme.md                   - This file