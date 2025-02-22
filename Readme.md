Tested with [Mu-Silicium](https://github.com/Project-Silicium/Mu-Silicium):

- **dtbs** extracted from **boot.img** work.
    
- **dtbs** dumped from `/sys/firmware/fdt` do **not** work (starts download mode with Samsung logo background instead of booting).
    
- **dtb** from the current work is **not** tested.
    

Tested with the default method using the [Mainline kernel](https://github.com/sm6115-mainline/linux) (packing into **boot.img**):

- **dtbs** extracted from **boot.img** cause bootloops (they are not rejected by **abl**, I think).
    
- **dtbs** dumped from `/sys/firmware/fdt` are **not** tested.
    
- **dtb** from the current work does **not** work (download mode with Samsung boot logo background).
    

I tried changing compatibility values in the dumped **dtbs**, but it did **not** work. I think **abl** requires some specific nodes in the **dtb**.