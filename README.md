# Iceriver Overclocking

We have so many people to thank for contributing to this project and are working on a complete contributor list and will update soon.  

While we did this out of excessive nerdy drive to learn and poke, we are not charging for this information or the modded binaries. Donations are always welcome and appreciated, but not necessary.  If you would like to donate, please send KAS to the following address:
`kaspa:qq3jzvq6jlapzjhngfj6m28cs8uq4ha47kcazauaaxt5ethw56p0xpq7pwnfa`

## Note worthy info about Iceriver ASIC miners
    User on each iceriver: bgchris168, root
    SSH port: 48699
    TCF/debug port: 1534

-----------------------------------------

# 1. Setting up your ASICs for remote access using Eclipse IDE
### To get connected:
1. Download and install eclipse https://www.eclipse.org/downloads/download.php?file=/technology/epp/downloads/release/2023-09/Reclipse-java-2023-09-R-win32-x86_64.zip&r=1
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

You should now be connected to the debug interface of the miner. 
You can view information or browse/edit files on the filesystem at your leisure. 

If you want an easy shell:
 - Edit the `/etc/shadow` file and find user `bgchris168`. 
 - Replace `$6$6are2S2fRbvF580O$ZFI9YBCaL8K1WCyoW71EyNGjZyjjMd9gQFrkh/q3tvJWM/hOj4733n/5TdXJWYLaUbBOwbiXOsmXxjmNmHb3/` with  `$6$6are2S2fRbvF580O$iFg2VSrSsacngl0SdG10huGL8fRIKz9/BDrRGktGpDWqPSuMXw0vV8mvih2TQcKJZRpLxwzw004S3V4MORmJ7/`.  
 - The password for `bgchris168` will be `password`.  Now you can ssh into your miner on port 48699.  

To have root privileges: 
 - Edit the `/etc/sudoers` file, find `root ALL=(ALL) ALL` and add a new line below it with `bgchris168 ALL=(ALL:ALL) ALL`.  
 - Now you can use `sudo su` to get root privileges using the above provided password.

**Note**: Please remember to backup the shadow and sudoers files incase its important and replace it afterwards. 

-----------------------------------------
