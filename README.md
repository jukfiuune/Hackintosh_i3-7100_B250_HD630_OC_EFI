# Hackintosh_i3-7100_B250_HD630_OC_EFI
This repo is a modified and updated version of this EFI: 
https://github.com/beyondgary/Hackintosh_i5-7500_B250_HD630_EFI 
Tested on Big Sur and Ventura.


## Hardware & System

| Name | Model Version |
| -------- | ----------------------------- |
| Motherboard | Gigabyte B250M-D3H |
| CPU | Intel i3 7100 |
| Graphics | Intel HD Graphics 630 |
| Sound Card | ALC892 |
| NIC | i219-v |
| SSD | Intel SSD with SATA interface |
| System | macOS Ventura 13.3.1 |
| Bootstrap | OpenCore 0.9.1 |
| Models | iMac18,1, iMac18,2, iMac18,3 | 

## BIOS settings

### `Gigabyte B250M-D3H` motherboard
Items in bold are mandatory.
- `M.I.T`
- `Miscellaneous Settings`
   - **`CFG Lock` = `Disabled`**
- `BIOS`
   - **`Fast Boot` = `Disabled`**
   - `Windows 8/10 Features` = `Windows 8/10`
   - **`CSM Support` = `Disabled`**
- `Peripherals`
   - `Initial Display Output` = `IGFX`
   - **`SW Guard Extensions (SGX)` = `Disabled`**
   - `Super IO Configuration`
     - `Serial Port` = `Disabled`
     - `Parallel Port` = `Disabled`
   - `USB Configuration`
     - **`Legacy USB Support` = `Enabled`**
     - **`XHCI Hand-off` = `Enabled`**
   - `SATA And RST Configuration`
     - **`SATA Mode Selection` = `AHCI`**
- `Chipset`
   - **`VT-d` = `Disabled`**
   - `Internal Graphics` = `Enabled`
   - `DVMT Pre-Allocated` = `64M`
   - `DVMT Total Gfx Mem` = `256M`

## Known Issues

* Unable to sleep, it will automatically wake up immediately after sleep, 
for a temporary solution use the following command to prevent entering 
sleep 
mode:
   ``` bash
   sudo pmset -a disablesleep 1
   ```
   When this value is set to 1, all sleep functions are disabled. The 
Sleep item in the Apple menu is also dimmed ("grayed out"). When set to 0, 
the sleep functionality will be restored.
  
