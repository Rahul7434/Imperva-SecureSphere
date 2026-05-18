Architecture:

```
Database Server
    |
[Imperva Agent] <--(Installed on DB server - windows/linux) 
    |
[Imperva Gateway]
    |
[Management server (MX)]

-Agent lives on DB server
-Agent send traffic to gateway
-MX controls policies, update, monitoring

```

Pre-requisites:
```
-Root/admin access
-Outbound connectivity to gateway (port usually 443)
-Time sync (NTP
-Enough Disk Space
```
Imperva Agent Installation on windows os for mssql:
```
1. Connectivity check on Gateway server & DB server for port 5555 and 443
(5555 required for data communication between the SecureSphere Agent and the gateway.
| and 443 for Allows firewall access for SecureSphere Agent management communication with the gateway )

2. Check the DB version and os version then check the compatible agent on from imperva release note portal (https://www.imperva.com/data-security-coverage-tool/) and download the agent zip file from ftp and upload it on db server.

3.Open CMD as administrator and go to the path where imperva package uploaded.

4.First install the R-agent then go for the installer installation.
- Go for "Quick Configuration" select 1 option  there will be another 2nd one option "Custome Advanced configuration"
-Shoud be traffic be monitored true/false
    -select true enter 1
-Enter the remote agent name : give the Hostname of DB server
-Enter the Gateway Ip or Hostname
-You can change the settings in the agent data interface tab in the GUI.
    -select both option 2
-Enter the gateway login password
-YOu will get the msg like "the initial configuration wizard was completed successfullly"
-Do you want to start the remote agent?
    -enter y


#### The now go to the reagentinstaller package file path
- 1) Quick Configuration 2) Custome Advanced configuration
    - Enter 1 for quicj configuration




```




