<i>Semaine 3 : Applications métiers et bases de données</i>

## 1. GLPI - Système de gestion de parc informatique et de helpdesk.

GLPI étant déjà installé sur mon système, je vérifie juste l'accès au service ainsi qu'a sa base de données.

<img src="./assets/glpi.png" width="700">
<br>

```
reqlu@ubuntu-glpi:~$ sudo mysql
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 52
Server version: 8.0.35-0ubuntu0.22.04.1 (Ubuntu)

Copyright (c) 2000, 2023, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current input statement.

mysql> SHOW DATABASES;
+--------------------+
| Database           |
+--------------------+
| TC2_test           |
| db2023_glpi        |
| information_schema |
| mysql              |
| ocsdb              |
| performance_schema |
| sys                |
| tournoi_foot       |
+--------------------+
8 rows in set (0,00 sec)

mysql> use db2023_glpi;
Reading table information for completion of table and column names
You can turn off this feature to get a quicker startup with -A


Database changed
mysql> 
mysql> SHOW TABLES;
+----------------------------------------------------------+
| Tables_in_db2023_glpi                                    |
+----------------------------------------------------------+
| glpi_agents                                              |
| glpi_agenttypes                                          |
| glpi_alerts                                              |
| glpi_apiclients                                          |
| glpi_applianceenvironments                               |
| glpi_appliances                                          |
| glpi_appliances_items                                    |
| glpi_appliances_items_relations                          |
| glpi_appliancetypes                                      |
| glpi_authldapreplicates                                  |
| glpi_authldaps                                           |
| glpi_authmails                                           |
| glpi_autoupdatesystems                                   |
| glpi_blacklistedmailcontents                             |
```

ss
