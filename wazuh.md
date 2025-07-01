# 🛡️ Wazuh SIEM Setup – Ubuntu + Windows Agent


## ✅ Requirements

- Ubuntu
- Windows (for agent)

---

1. Install Wazuh All-in-One on Ubuntu

```bash
curl -sO https://packages.wazuh.com/4.7/wazuh-install.sh
sudo bash wazuh-install.sh -a
```

2. Open Firewall Ports
3. ```
   sudo ufw allow 1514/udp    
   sudo ufw allow 1515/tcp
4. Once installed, open your browser enter your ip address
5. enter the username and password that is given in your terminal while installing processing of wazuh


# Configure Windows Agent
1.download wazuh agent


[download link](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/wazuh-agent-package-windows.html)


2.install the agent


3.open powershell as administrator


```bash
cd "C:\Program Files (x86)\ossec-agent"
notepad ossec.conf
```
```
<client>
  <server>
    <address>192.168.1.6</address> #change the ip as per your ip in ubuntu server
    <port>1514</port>
    <protocol>udp</protocol>
  </server>
</client>
```
```
.\agent-auth.exe -m 192.168.1.6 # your ubuntu server ip

```
now the agent should be connected to the server




for more references
[visit wazuh offical documentation](https://documentation.wazuh.com/current/installation-guide/wazuh-agent/wazuh-agent-package-windows.html)
