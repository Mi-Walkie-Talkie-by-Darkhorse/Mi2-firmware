## About
**Mi2-firmware** project is a collection of Xiaomi Mi Walkie-Talkie 2 (MJDJJ02FY) firmware files with the related disassembler databases.  
All the reverse-engeneering operations were performed using [IDA](https://www.hex-rays.com/products/ida/overview.shtml) 6.8 disassembler; all the .idb files in the project are the IDA 6.8 Databases, and all the .idc files are the IDA scripts.  
All the .bin firmware files are the standard Mi Walkie-Talkie firmware packages, and could be explored using [fwinfo](https://github.com/Mi-Walkie-Talkie-by-Darkhorse/fwinfo) tool.
 
 ## Project structure
* **firmware-original** - original MJDJJ02FY firmware files, with the related disassembler databases (only the CPU firmware section has been disassembled!).
* **firmware-mod-nolimits** - modified MJDJJ02FY firmware, which allows to use an entire walkie-talkie radio chip frequency range 130-520MHz without any redundant software limitations (the actual frequency range, though, is limited by the radio circuitry and could vary from one radio to another). Use [Mi-Walkie-Talkie-Plus](https://github.com/Mi-Walkie-Talkie-by-Darkhorse/Mi-Walkie-Talkie-Plus/edit/2.9.34-plus) Android app mod to flash the modified firmware, and to set any frequency you want for the user channels. .idc files in the folder are IDA scripts to patch the original firmware, producing "nolimits" mod; you can apply these scripts to the corresponding database by opening .idb file with IDA, pressing "Alt-F7", and selecting the .idc you want.
