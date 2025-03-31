# How to install Elastic Seach from archive

## Download and install archive for linux
`$ wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.17.4-linux-x86_64.tar.gz`

`$ wget https://artifacts.elastic.co/downloads/elasticsearch/elasticsearch-8.17.4-linux-x86_64.tar.gz.sha512`

`$ shasum -a 512 -c elasticsearch-8.17.4-linux-x86_64.tar.gz.sha512`

`$ tar -xzf elasticsearch-8.17.4-linux-x86_64.tar.gz`

`$ cd elasticsearch-8.17.4/`
### move to /usr/share/elasticsearch
`$ mkdir /usr/share/elasticsearch`

`$ mv elasticsearch-8.17.4/** /usr/share/elasticsearch`

## add to PATH
##### add to the end of the file ~/.bashrc
`$ export PATH=$PATH:/usr/share/elasticsearch/bin`

## To run elasticsearch
`$ elasticsearch`
