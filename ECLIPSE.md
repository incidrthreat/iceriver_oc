## Note worthy info about Iceriver ASIC miners
    User on each iceriver: bgchris168, root
    SSH port: 48699
    TCF/debug port: 1534

-----------------------------------------

# 1. Setting up your ASICs for remote access using Eclipse IDE
### To get connected:
1. Download and install eclipse https://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/2023-09/R/eclipse-java-2023-09-R-win32-x86_64.zip&r=1
2. Start eclipse
3. Go to Help -> Install new Software
4. in the work with field enter: https://download.eclipse.org/tools/tcf/releases/1.7/1.7.0
5. Click add 
6. Give it a name 
7. Click add
8. Select "Target Communication Framework" and "TCF Target Explorer" 
9. Click next and agree to the license, click finish 
10. Restart eclipse when prompted 
11. When eclipse restarts along the top bar there should be a new option for "New Connection" 
12. Click "New Connection"
13. Select Generic Connection 
14. For Connection Name click browse
15. The IP of the miner should appear as a tcf agent  
16. Select the ip 
17. Click OK 
18. Click Finish 
19. Proceed to the next section:
    - 19a. If you are using a KS0, go to [KS0 Overclocking](./KS0/README.md)
    - 19b. If you are using a KS1, go to [KS1 Overclocking](./KS1/README.md)
    - 19c. If you are using a KS2, go to [KS2 Overclocking](./KS2/README.md)
    - 19d. If you are using a KS3L, go to [KS3L Overclocking](./KS3L/README.md)

You should now be connected to the debug interface of the miner. 
You can view information or browse/edit files on the filesystem at your leisure. 

If you want an easy shell:
 - Edit the `/etc/shadow` file and find user `bgchris168`. 
 - Replace `$6$6are2S2fRbvF580O$ZFI9YBCaL8K1WCyoW71EyNGjZyjjMd9gQFrkh/q3tvJWM/hOj4733n/5TdXJWYLaUbBOwbiXOsmXxjmNmHb3/` with  `$6$6are2S2fRbvF580O$iFg2VSrSsacngl0SdG10huGL8fRIKz9/BDrRGktGpDWqPSuMXw0vV8mvih2TQcKJZRpLxwzw004S3V4MORmJ7/`  
 - The password for `bgchris168` will be `password`.  Now you can ssh into your miner on port 48699.  

To have root privileges: 
 - Edit the `/etc/sudoers` file, find `root ALL=(ALL) ALL` and add a new line below it with `bgchris168 ALL=(ALL:ALL) ALL`.  
 - Now you can use `sudo su` to get root privileges using the above provided password.

**Note**: Please remember to backup the shadow and sudoers files incase its important and replace it afterwards.