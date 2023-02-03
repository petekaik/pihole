# Pi-hole

Simple Pi-hole adblocker setup based on jacklul/pihole:latest with additional black and whitelists - Parametrable via .env file or other environment variable mechanisms

Initiate by creating a macvlan network on Docker host: If your LAN is in 192.168.1.0/24 space and your router/gateway IP is 192.168.1.1, the following command would create suitable LAN exposed network in which you can give Pi-hole container a 192.168.1.x address:

docker network create -d macvlan --subnet=192.168.1.0/24 --gateway=192.168.1.1 -o parent=eth0 physical_eth0

(replace "parent=eth0" with your physical ethernet interface and the last "physical_eth0" with whatever you want Docker internal network to call this newly created network interface)

Remember to run "Tools > Update Gravity" after first launch
