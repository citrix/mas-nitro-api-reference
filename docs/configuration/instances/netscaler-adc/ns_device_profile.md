#ns_device_profile



Configuration for ns_device_profile resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Profile Name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>svm_ns_comm</td><td>&lt;String></td><td>Read-write</td><td>Communication with Instances.<br>Minimum length = 1<br>Maximum length = 10</td></tr><tr><td>use_global_setting_for_communication_with_ns</td><td>&lt;Boolean></td><td>Read-write</td><td>True, if the communication with Instance needs to be global and not device specific.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the device profiles.</td></tr><tr><td>is_default</td><td>&lt;Boolean></td><td>Read-write</td><td>True, if this profile is system generated and can not be deleted.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Profile Type, This must be with in specified supported profiles (NS / Xen).<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant Id of device profile.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>snmpsecurityname</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 security name for this profile.<br>Maximum length = 31</td></tr><tr><td>snmpauthprotocol</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 auth protocol for this profile.</td></tr><tr><td>ssl_private_key</td><td>&lt;String></td><td>Read-write</td><td>SSL Private Key for key based authentication.</td></tr><tr><td>wait_time_after_reboot</td><td>&lt;String></td><td>Read-write</td><td>Wait time after reboot in seconds.</td></tr><tr><td>ssl_cert</td><td>&lt;String></td><td>Read-write</td><td>SSL Certificate for certificate based authentication.</td></tr><tr><td>ns_profile_name</td><td>&lt;String></td><td>Read-write</td><td>Profile Name, This is one of the already created NetScaler profiles.</td></tr><tr><td>ssh_port</td><td>&lt;String></td><td>Read-write</td><td>SSH port to connect to the device.</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password for this profile.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>snmpsecuritylevel</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 security level for this profile.</td></tr><tr><td>snmpcommunity</td><td>&lt;String></td><td>Read-write</td><td>SNMP community for this profile.<br>Maximum length = 31</td></tr><tr><td>passphrase</td><td>&lt;String></td><td>Read-write</td><td>Passphrase with which private key is encrypted.</td></tr><tr><td>snmpprivprotocol</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 priv protocol for this profile.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>User Name for this profile.<br>Minimum length = 1<br>Maximum length = 127</td></tr><tr><td>snmpprivpassword</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 priv password for this profile.<br>Minimum length = 8<br>Maximum length = 31</td></tr><tr><td>snmpversion</td><td>&lt;String></td><td>Read-write</td><td>SNMP version for this profile.</td></tr><tr><td>snmpauthpassword</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 auth password for this profile.<br>Minimum length = 8<br>Maximum length = 31</td></tr><tr><td>cb_profile_name</td><td>&lt;String></td><td>Read-write</td><td>Profile Name, This is one of the already created NetScaler SD-WAN profiles.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_device_profile?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_device_profile: {
<b>"name":<String_value></b>,
<b>"password":<String_value></b>,
<b>"username":<String_value></b>,
"wait_time_after_reboot":<String_value>,
"ssl_private_key":<String_value>,
"snmpauthprotocol":<String_value>,
"snmpsecurityname":<String_value>,
"svm_ns_comm":<String_value>,
"ssl_cert":<String_value>,
"ns_profile_name":<String_value>,
"use_global_setting_for_communication_with_ns":<Boolean_value>,
"ssh_port":<String_value>,
"tenant_id":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"passphrase":<String_value>,
"id":<String_value>,
"is_default":<Boolean_value>,
"snmpprivprotocol":<String_value>,
"snmpprivpassword":<String_value>,
"type":<String_value>,
"snmpversion":<String_value>,
"cb_profile_name":<String_value>,
"snmpauthpassword":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_device_profile":[{
"name":<String_value>,
"svm_ns_comm":<String_value>,
"use_global_setting_for_communication_with_ns":<Boolean_value>,
"id":<String_value>,
"is_default":<Boolean_value>,
"type":<String_value>,
"tenant_id":<String_value>,
"snmpsecurityname":<String_value>,
"snmpauthprotocol":<String_value>,
"ssl_private_key":<String_value>,
"wait_time_after_reboot":<String_value>,
"ssl_cert":<String_value>,
"ns_profile_name":<String_value>,
"ssh_port":<String_value>,
"password":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"passphrase":<String_value>,
"snmpprivprotocol":<String_value>,
"username":<String_value>,
"snmpprivpassword":<String_value>,
"snmpversion":<String_value>,
"snmpauthpassword":<String_value>,
"cb_profile_name":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_device_profile/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_device_profile

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_device_profile":[{
"name":<String_value>,
"svm_ns_comm":<String_value>,
"use_global_setting_for_communication_with_ns":<Boolean_value>,
"id":<String_value>,
"is_default":<Boolean_value>,
"type":<String_value>,
"tenant_id":<String_value>,
"snmpsecurityname":<String_value>,
"snmpauthprotocol":<String_value>,
"ssl_private_key":<String_value>,
"wait_time_after_reboot":<String_value>,
"ssl_cert":<String_value>,
"ns_profile_name":<String_value>,
"ssh_port":<String_value>,
"password":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"passphrase":<String_value>,
"snmpprivprotocol":<String_value>,
"username":<String_value>,
"snmpprivpassword":<String_value>,
"snmpversion":<String_value>,
"snmpauthpassword":<String_value>,
"cb_profile_name":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_device_profile/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_device_profile":[{
"name":<String_value>,
"svm_ns_comm":<String_value>,
"use_global_setting_for_communication_with_ns":<Boolean_value>,
"id":<String_value>,
"is_default":<Boolean_value>,
"type":<String_value>,
"tenant_id":<String_value>,
"snmpsecurityname":<String_value>,
"snmpauthprotocol":<String_value>,
"ssl_private_key":<String_value>,
"wait_time_after_reboot":<String_value>,
"ssl_cert":<String_value>,
"ns_profile_name":<String_value>,
"ssh_port":<String_value>,
"password":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"passphrase":<String_value>,
"snmpprivprotocol":<String_value>,
"username":<String_value>,
"snmpprivpassword":<String_value>,
"snmpversion":<String_value>,
"snmpauthpassword":<String_value>,
"cb_profile_name":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_device_profile/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_device_profile:{
<b>"id":<String_value></b>,
"wait_time_after_reboot":<String_value>,
"ssl_private_key":<String_value>,
"snmpauthprotocol":<String_value>,
"snmpsecurityname":<String_value>,
"svm_ns_comm":<String_value>,
"ssl_cert":<String_value>,
"ns_profile_name":<String_value>,
"use_global_setting_for_communication_with_ns":<Boolean_value>,
"ssh_port":<String_value>,
"password":<String_value>,
"tenant_id":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"passphrase":<String_value>,
"is_default":<Boolean_value>,
"name":<String_value>,
"snmpprivprotocol":<String_value>,
"username":<String_value>,
"snmpprivpassword":<String_value>,
"type":<String_value>,
"snmpversion":<String_value>,
"cb_profile_name":<String_value>,
"snmpauthpassword":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_device_profile":[{
"name":<String_value>,
"svm_ns_comm":<String_value>,
"use_global_setting_for_communication_with_ns":<Boolean_value>,
"id":<String_value>,
"is_default":<Boolean_value>,
"type":<String_value>,
"tenant_id":<String_value>,
"snmpsecurityname":<String_value>,
"snmpauthprotocol":<String_value>,
"ssl_private_key":<String_value>,
"wait_time_after_reboot":<String_value>,
"ssl_cert":<String_value>,
"ns_profile_name":<String_value>,
"ssh_port":<String_value>,
"password":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"passphrase":<String_value>,
"snmpprivprotocol":<String_value>,
"username":<String_value>,
"snmpprivpassword":<String_value>,
"snmpversion":<String_value>,
"snmpauthpassword":<String_value>,
"cb_profile_name":<String_value>}]}
```







