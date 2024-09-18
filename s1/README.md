***Semaine 1***

*1. Infrastructure*
**pour commencer, voici l'architecture du serveur sur lequel mes services d'administration tournerons:**
[img -uname ]

On commence par mettre à jour nos dépôts
```apt update && apt upgrade -y```

## 1. Kibana & ElasticSearch

```
s1-elk@s1-elk:~$ wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add -
[sudo] password for s1-elk: 
Warning: apt-key is deprecated. Manage keyring files in trusted.gpg.d instead (see apt-key(8)).
OK
s1-elk@s1-elk:~$ sudo apt-get install apt-transport-https
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  apt-transport-https
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 1510 B of archives.
After this operation, 170 kB of additional disk space will be used.
Get:1 http://archive.ubuntu.com/ubuntu jammy-updates/universe amd64 apt-transport-https all 2.4.13 [1510 B]
Fetched 1510 B in 0s (5019 B/s)               

```

```
s1-elk@s1-elk:~$ echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" | sudo tee -a /etc/apt/sources.list.d/elastic-7.x.list
deb https://artifacts.elastic.co/packages/7.x/apt stable main
s1-elk@s1-elk:~$
```

```
s1-elk@s1-elk:~$ sudo apt-get install elasticsearch -y
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  elasticsearch
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 326 MB of archives.
```

```
s1-elk@s1-elk:~$ sudo apt install kibana
Reading package lists... Done
Building dependency tree... Done
Reading state information... Done
The following NEW packages will be installed:
  kibana
0 upgraded, 1 newly installed, 0 to remove and 0 not upgraded.
Need to get 292 MB of archives.
After this operation, 746 MB of additional disk space will be used.
Get:1 https://artifacts.elastic.co/packages/7.x/apt stable/main amd64 kibana amd64 7.17.24 [292 MB]
Fetched 292 MB in 36s (8210 kB/s)                                                                                                                    
debconf: delaying package configuration, since apt-utils is not installed
Selecting previously unselected package kibana.
(Reading database ... 65308 files and directories currently installed.)
Preparing to unpack .../kibana_7.17.24_amd64.deb ...
Unpacking kibana (7.17.24) ...


Setting up kibana (7.17.24) ...
Creating kibana group... OK
Creating kibana user... OK

```
