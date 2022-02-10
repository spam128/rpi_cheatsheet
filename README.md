STARTUP for wifi
-------

Prepare sd card

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


Connect to rpi 

- Find rpi ip addres or use advanced ip scanner:
 run (all raspberry pi mac starts from b8-27-eb) 
`arp -a | grep b8-27-eb`



- connect through ssh

defaul login: pi
default password: raspberry
