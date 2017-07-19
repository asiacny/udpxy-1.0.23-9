# udpxy-1.0.23-9
modified udpxy to secure status page, you can now enter status page only from specific IP or not

# install instructions:
- sudo apt-get install build-essentials
- git clone https://github.com/seevik2580/udpxy-1.0.23-9.git
- cd udpxy-1.0.23-9
- make
- make install

# usage example:
##### run udpxy with public /status & /restart page, public stream
- udpxy				

##### run udpxy with stricted access to /status & /restart page, only specific IP can enter, public stream
- UDPXY_MNGIP=192.168.1.1 udpxy	

