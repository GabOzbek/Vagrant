Oracle Express Edition 11g Release 2 on Ubuntu 14.04.1 LTS
============================

### Installation

# Hämta ner image
docker pull wnameless/oracle-xe-11g

# Exekvera med port 22 and 1521
docker run --name oracle -d -p 49160:22 -p 49161:1521 wnameless/oracle-xe-11g

# Logga in i db
hostname: localhost
port: 49161
sid: xe
username: system
password: oracle


# Strunta i det som är här nere
------------------------
Lösenord för SYS & SYSTEM
oracle

Logga in med SSH
ssh root@localhost -p 49160
password: admin

