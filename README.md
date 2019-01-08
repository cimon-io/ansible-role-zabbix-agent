Zabbix agent role
-----------------

An Ansible role that installs zabbix agent.

Role Variables
--------------

Available variables are listed below, along with default values (see defaults/main.yml):

```
zabbix_service_enabled: yes
zabbix_version: 3.4

zabbix_PidFile: "/tmp/zabbix_agentd.pid"
zabbix_LogType: "file"
zabbix_LogFile: ""
zabbix_LogFileSize: 1
zabbix_DebugLevel: 3
zabbix_SourceIP: ""
zabbix_EnableRemoteCommands: 0
zabbix_LogRemoteCommands: 0
zabbix_Server: ""
zabbix_ListenPort: 10050
zabbix_ListenIP: "0.0.0.0"
zabbix_StartAgents: 3
zabbix_ServerActive: ""
zabbix_Hostname: ""
zabbix_HostnameItem: "system.hostname"
zabbix_HostMetadata: ""
zabbix_HostMetadataItem: ""
zabbix_RefreshActiveChecks: 120
zabbix_BufferSend: 5
zabbix_BufferSize: 100
zabbix_MaxLinesPerSecond: 20
zabbix_Timeout: 3
zabbix_AllowRoot: 0
zabbix_User: "zabbix"
zabbix_Include: ""
zabbix_UnsafeUserParameters: 0
zabbix_UserParameter: ""
zabbix_LoadModulePath: "${libdir}/modules"
zabbix_LoadModule: ""
zabbix_TLSConnect: "unencrypted"
zabbix_TLSAccept: "unencrypted"
zabbix_TLSCAFile: ""
zabbix_TLSCRLFile: ""
zabbix_TLSServerCertIssuer: ""
zabbix_TLSServerCertSubject: ""
zabbix_TLSCertFile: ""
zabbix_TLSKeyFile: ""
zabbix_TLSPSKIdentity: ""
zabbix_TLSPSKFile: ""
```

---

Host autoregistration:

```
zabbix_Hostname: "{{ zabbix_group }}.{{ inventory_hostname_short }}"
zabbix_HostMetadata: "{{ zabbix_group }} {{ zabbix_token }}"
```
