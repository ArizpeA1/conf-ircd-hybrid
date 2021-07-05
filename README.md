# conf-ircd-hybrid
Installation instructions and Configuration files for Ircd-hybrid server on debian 11

## Install and preparation
Make sure you don't have any ircd server with netstat
    
    netstat -tulpn
    
If any irc program is listening on ports 6665-6669 remove it to make sure ircd-hybrid doesn't have any problems
For installing ircd-hybrid just run:
    
    sudo apt-get install ircd-hybrid

