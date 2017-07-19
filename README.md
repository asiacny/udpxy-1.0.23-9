# udpxy-1.0.23-9
- [udpxy](https://github.com/pcherenkov/udpxy) is a UDP-to-HTTP multicast traffic relay daemon it forwards UDP traffic from a given multicast subscription to the requesting HTTP client
-udpxy is released under GPL v.3

- this modified version of udpxy with secured status page, you can now enter status page both ways, only from specific IP or from everywhere. defined by enviroment variable UDPXY_MNGIP

# install instructions:
- sudo apt-get install build-essentials
- git clone https://github.com/seevik2580/udpxy-1.0.23-9.git
- cd udpxy-1.0.23-9
- make
- make install

# usage example:
##### udpxy help usage
- udpxy -h

##### run udpxy with public /status & /restart page, public stream
- udpxy	-someparameters			

##### run udpxy with stricted access to /status & /restart page, only specific IP can enter, public stream
- UDPXY_MNGIP=192.168.1.1 udpxy	-someparameters

