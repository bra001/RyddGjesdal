# Remote Desktop setup from fresh image
**Freshly imaged Rasbian on SD**
Create a file named "ssd" into boot (it's the only dir visible in FIle Explorer)
Create file named "wpa_supplicant.conf" with following content:

"""
ctrl_interface=DIR=/var/run/wpa_supplicant GROUP=netdev
update_config=1
country=US

network={
	ssid="your-network-service-set-identifier"
	psk="your-network-WPA/WPA2-security-passphrase"
	key_mgmt=WPA-PSK
}
"""

Find your raspberry ip-address

SSH into raspberry
'''
uname: pi
passw: raspberry
'''

'''
sudo apt-get remove xrdp vnc4server tightvncserver

sudo apt-get install tightvncserver

sudo apt-get install xrdp
'''

Connect to device using Remote Desktop
