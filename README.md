# Crowd LDAP Server

Implementation of an LDAP server that delegates authentication to an Atlassian Crowd installation
using the Crowd REST API. 

This service allows your favourite SSO authentication source to be used from many legacy devices, appliances and systems.

The LDAP implementation is based on the Apache Directory Server v1.5.7,  which is distributed under the Apache v2.0 License.

# How to build
```bash
docker run -d --rm --name ldap-builder maven:3.3-jdk-8 -- tail -f /dev/null
docker exec -it ldap-builder bash
apt-get update
apt-get install -y git
git clone https://github.com/dwimberger/crowd-ldap-server
cd crowd-ldap-server
mvn install -Dmaven.test.skip=true
```
