STARTUP for wifi
-------

Prepare sd card
- Write operating system on card

etcher to write (don't use dd it can be unpredictable)
https://www.balena.io/etcher/

raspbian images
https://www.raspberrypi.com/software/operating-systems/

- Create empty file `ssh` to allow ssh connection

- Create wpa_supplicant.conf and add (change network name and password)
```
country=PL
update_config=1
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
 
network={ 
    ssid="network_name" 
    psk="password" 
    key_mgmt=WPA-PSK 
}
```

- append your public key `~/.ssh/id_rsa.pub` to sd card authorized_keys `.ssh/authorized_keys`


Connect to rpi 

- Find rpi ip addres or use advanced ip scanner:
 run (all raspberry pi mac starts from b8-27-eb) 
`arp -a | grep b8-27-eb`



- connect through ssh

defaul login: pi
default password: raspberry


Interesting project
-------------------

balena-rpiplay
Turn a Raspberry Pi into an Airplay server using RPiPlay to enable screen mirroring on tvs, monitors and projectors.

This project essentially creates a docker image wrapping RPiPlay and making it easily deployable to balena fleets.
