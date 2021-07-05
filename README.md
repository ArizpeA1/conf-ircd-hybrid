# conf-ircd-hybrid
Installation instructions and Configuration files for Ircd-hybrid server on debian 11

## Install and preparation
Make sure you don't have any ircd server with netstat
    
    sudo netstat -tulpn
    
If any irc program is listening on ports 6665-6669 remove it to make sure ircd-hybrid doesn't have any problems
For installing ircd-hybrid just run:
    
    sudo apt-get install ircd-hybrid

after it is done clone the ircd.conf file
## Configuring (as root)
For making a backup of the auto-generated conf file 

    mv /etc/ircd-hybrid/ircd.conf /etc/ircd-hybrid/ircd-original.config
    
 now copy the file downloaded earlier to
 
    cp /path/to/cloned/ircd.conf /etc/ircd-hybrid/ircd.conf
    
and edit it:

    vim /etc/ircd-hybrid/ircd.conf
 
 after you're done to acticate the server
 
    systemctl enable ircd-hybrid
    service start ircd-hybrid
  
 ## Notes
 edit what you need to edit in the file, to get the ip adresess run
 
    ip a
    
 to generate the password run
 
    mkconfig
 
