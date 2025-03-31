# How to install elasticsearch using from archive

## Download and install archive for Linux
### cd first to targeted directory: eg: cd ~/Downloads
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.17.4-linux-x86_64.tar.gz
wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.17.4-linux-x86_64.tar.gz.sha512
shasum -a 512 -c elasticsearch-8.17.4-linux-x86_64.tar.gz.sha512
tar -xzf elasticsearch-8.17.4-linux-x86_64.tar.gz
cd elasticsearch-8.17.4/
### or move to /usr/share/elasticsearch
mkdir /usr/share/elasticsearch
mv elasticsearch-8.17.4/** /usr/share/elasticsearch

## set up the bin
sudo nano ~/.bashrc
## add this at the end of the line
export PATH=$PATH:/usr/share/elasticsearch/bin

## You can run elastic search by
$ elasticsearch

## IMPORTANT SETTINGS
### PATH SETTINGS
