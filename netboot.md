1. Open pfsense
2. System/Package manager/available packages -> tftp
3. Services/TFTP server/Enable
4. TFTP server/files/
    4.1 Download to local disk then upload it https://boot.netboot.xyz/ipxe/netboot.xyz.efi 
    4.2 Download to local disk then upload it https://boot.netboot.xyz/ipxe/netboot.xyz-arm64.efi
5. Services/DHCP server/TFTP server - set it to your DHCP server's IP address (most likely router's IP)
6. Services/DHCP server/Network Booting - `Enable`
    6.1 Next Server - set it to your DHCP server's IP address (most likely router's IP)
    6.4 UEFI 64bit - `netboot.xyz.efi`
    6.5 ARM 64 bit - `netboot.xyz-arm64.efi`
    6.6 Root path - `/tftpboot/`
7. Save all, and boot up a machine and select PXE boot option
