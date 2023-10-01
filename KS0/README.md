# Iceriver KS0 Overclocking

**Before proceeding, please read the [disclaimer](../DISCLAIMER.md)**

# Option 1 - update via the webgui
1. Grab the updated file [update.bgz](./files/update.bgz)
    - SHA256: `DB3653235160DAA18FC051A90E065B99E8D067D390EB9FF718B6883E2DE7A826 update.bgz`
2. Navigate to webgui - Firmware Upgrade page
3. Select the update.bgz file and from your local machine and click update.
4. Follow the prompts to reboot.
5. After about 2-5 minutes the webgui should be accessible again.  Miner hashrate will range bw 140-160 GH/s depending on silicon lottery.

# Option 2 - update via Eclipse IDE
1. Upgrade to the latest KS0 firmware from Iceriver by downloading from [here](https://file1.iceriver.io/firmware/ks0_firmware_please%20unzip%20before%20upgrading.zip).
2. Once the miner has rebooted and Eclipse IDE has reconnected, head over to File System tab below.  
3. Navigate to `/var/update` and delete `miner.bgz`. 
4. Upload by dragging/dropping the modified [miner.bgz](./files/miner.bgz) provided into the `/var/update` folder.  
    - SHA256: `DBE03CC291E2F9047FF8765F4638DE3933B698357F953EC3D6C9E85B567E0B78  miner.bgz`
5. Once the transfer is complete, reboot via SSH, Webgui, or the good 'ol fashion unplug/replug method.
6. After about 2-5 minutes the webgui should be accessible again.  Miner hashrate will range bw 140-160 GH/s depending on silicon lottery.

**Additional warning for those using this overclock, ensure you have the proper power supply to handle the increased power draw.  Some of the stock PSUs provided with the KS0 are not capable of handling the increased power draw. It is recommended to have at the very least 120w power supply.**

----------------------------
Below are a few links to some power supplies that have been tested and confirmed to work with the KS0 Overclock.
- Laptop charger for Asus 180w 19.5v - https://amzn.to/3REhwLC
- Laptop charger for Asus 150w 19.5v - https://amzn.to/3PYqEcX
- Laptop charger for MSI 150w 19.5v - https://amzn.to/3Pwy1Xw