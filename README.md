# SURICATA Ruleset and enviroment setup
This repo contains simple ruleset and enviroment setup to conduct simple SURICATA of PKAP or various network resources
## What is Suricata?
Suricata is a high performance, open source network analysis and threat detection software used as an IDS/IPS. 
Suricata offers alerts, network flows, PCAP recordings etc


Read more: https://suricata.io/

## How to use Suricata
1) Download suricata on your LINUX distro

   
Link: https://suricata.io/download/

```` bash
sudo apt install suricata
````
2) Ensure that suricata is downloaded properly
```` bash
sudo suricata --build-info 
````

3) Create a suricata ruleset file
```` bash
ls
cd suricata-test
nano suricata.rules
````

4) Write your ruleset in your suricata.rules file
This can be done through texteditor or nano/vim/vi

5) Create a yaml for enviroment setup
```` bash
nano suricata.yaml
````    

6) Write your enviroment properties in your suricata.yaml file
This can be done through texteditor or nano/vim/vi

7) Enter a suricata command in your cli to connect the ruleset, file you would like to search and yaml together
```` bash
sudo suricata -r path/to/yourfile.pcap -c path/to/suricata.yaml  -S path/to/file-download.rules -l path/to/output/dir
````
8) Result/Print will be visible in the json.log file 
   
