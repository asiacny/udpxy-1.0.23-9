# udpxy-1.0.23-9
- [udpxy](https://github.com/pcherenkov/udpxy) is a UDP-to-HTTP multicast traffic relay daemon it forwards UDP traffic from a given multicast subscription to the requesting HTTP client
- udpxy is released under GPL v.3

- this is modified version of udpxy with secured status page, you can now enter status page both ways, only from specific IP or from everywhere. defined by enviroment variable UDPXY_MNGIP

# install instructions:
- `sudo apt-get install build-essentials`
- `git clone https://github.com/seevik2580/udpxy-1.0.23-9.git`
- `cd udpxy-1.0.23-9`
- `make`
- `sudo make install`

# usage example:
##### udpxy help usage
- `udpxy`

##### run udpxy no daemon, with public /status & /restart page & public stream, client statistics, verbosed, listening on port 5555, input interface for HTTP requests is eth0, multicast interface for stream is eth1
- `udpxy	-T -S -v -p 5555 -a eth0 -m eth1`

##### run udpxy no daemon, with granted access to /status & /restart page only from IP 192.168.1.1, public stream, client statistics, verbosed, listening on port 5555, input interface for HTTP requests is eth0, multicast interface for stream is eth1
- `UDPXY_MNGIP=192.168.1.1 udpxy	-T -S -v -p 5555 -a eth0 -m eth1`

