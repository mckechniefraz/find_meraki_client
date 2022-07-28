# Find Meraki Client
## Purpose of this script
This script is built to search all networks within a given Meraki organisation to find all client devices which either fully or partially match a given IP. Once all networks have
been checked, the data is output into a table. 

## Install
Clone repository to local machine
````
git clone git@github.com:mckechniefraz/find_meraki_client.git
````
Create virtual environment and install requirements
````
python3 venv venv
source venv/bin/activate
pip3 install -r requirements.txt
````
## Usage
The script runs by accepting three arguments at run time, API Key, Org Id and the Client IP.
````
python3 meraki_device_searcher.py --key=qwerty12345 --o=123456 --i=10.0.0.89 
  networkName   clientIp   clientName   cleintMac           connectionType   firstSeen              lastSeen
0 Test_Network  10.0.0.89  Test_device  aa:bb:cc:dd:ff:ff    Wireless        2021-07-11T11:42:23Z  2022-07-24T16:08:06Z
````

### help output
````
usage: meraki_device_searcher.py [-h] [--k API Key] [--o Org ID] [--i Cleint IP]

Meraki Find Client Arguments

optional arguments:
  -h, --help     show this help message and exit
  --k API Key    API Key for Meraki Dashboard
  --o Org ID     Organisation ID for the Meraki Dashboard
  --i Cleint IP  Client IP you are searching for
````