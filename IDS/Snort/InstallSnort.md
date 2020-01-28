Requirements:

```
sudo apt-get install -y build-essential
sudo apt-get install -y libpcap-dev libpcre3-dev libdumbnet-dev
sudo apt-get install -y libnghttp2-dev
sudo apt-get install -y zlib1g-dev liblzma-dev openssl libssl-dev
sudo apt-get install -y bison flex
```
Install LuaJIT:
```
wget http://luajit.org/download/LuaJIT-2.0.5.tar.gz
make
sudo make install
sudo ln -s /usr/local/include/luajit-2.0/* /usr/local/include/
```
Install DAQ:
```
wget https://www.snort.org/downloads/snort/daq-2.0.6.tar.gz
tar -xvzf daq-2.0.6.tar.gz
cd daq-2.0.6
./configure
make
sudo make install
```

Install Snort:
```
wget https://www.snort.org/downloads/archive/snort/snort-2.9.15.1.tar.gz
tar -xvzf snort-2.9.15.1.tar.gz
cd snort-2.9.15.1
./configure --enable-sourcefire
make
sudo make install

snort -V
```