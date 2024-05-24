# pi-hole-setup
pi-hole-setup

1. installing Pi-Hole and assingning rasberry Pi a static IP
![image](https://github.com/DomDavis70/pi-hole-setup/assets/42983767/f698acd4-dc78-4afe-84c7-623d2f99a5df)

2. Used `route -n` to find the IP of the DHCP
These were the DHCP IP range and I changed the end address to 192.168.1.100 and assigned the Rasberry Pi outside of that.
DHCPv4 Start Address	192.168.1.64
DHCPv4 End Address	192.168.1.253

![image](https://github.com/DomDavis70/pi-hole-setup/assets/42983767/f79c1852-161f-425a-8006-1354cff7bcb9)

3. After cloning and installing Docker with this [link](https://github.com/pi-hole/docker-pi-hole), I needed to allow it to be run by non-root users using `sudo usermod -aG docker $USER`
Then start Docker by running ./docker_run.sh

4. You then need to open the dhcp config using `sudo nano /etc/dhcpcd.conf` and add the line `domain\_name\_servers=x.x.x.x` (replacing `x.x.x.x` with the IP address of your Pi-hole server)

5. 
