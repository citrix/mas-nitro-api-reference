#ns_snmp_config



Configuration for SNMP configuration resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>save_config</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if save config is required.</td></tr><tr><td>trapdestination</td><td>&lt;String></td><td>Read-write</td><td>State of configuration (enable/disable).</td></tr><tr><td>snmpauthprotocol</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 auth protocol.</td></tr><tr><td>snmpsecurityname</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 security name.<br>Maximum length = 31</td></tr><tr><td>snmpprivprotocol</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 priv protocol.</td></tr><tr><td>ns_ip_address_arr</td><td>&lt;String[]></td><td>Read-write</td><td>List of NS IP Address.<br>Maximum length = 64</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State of configuration (enable/disable).</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>snmpsecuritylevel</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 security level.</td></tr><tr><td>snmpcommunity</td><td>&lt;String></td><td>Read-write</td><td>SNMP community.<br>Maximum length = 31</td></tr><tr><td>snmpprivpassword</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 priv password.<br>Minimum length = 8<br>Maximum length = 31</td></tr><tr><td>snmpversion</td><td>&lt;String></td><td>Read-write</td><td>SNMP version.</td></tr><tr><td>snmpauthpassword</td><td>&lt;String></td><td>Read-write</td><td>SNMP v3 auth password.<br>Minimum length = 8<br>Maximum length = 31</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_snmp_config?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_snmp_config: {
<b>"ns_ip_address":<String_value></b>,
<b>"snmpversion":<String_value></b>,
"snmpsecurityname":<String_value>,
"snmpauthprotocol":<String_value>,
"state":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"save_config":<Boolean_value>,
"trapdestination":<String_value>,
"snmpprivprotocol":<String_value>,
"ns_ip_address_arr":<String_value[]>,
"snmpprivpassword":<String_value>,
"snmpauthpassword":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_snmp_config":[{
"save_config":<Boolean_value>,
"trapdestination":<String_value>,
"snmpauthprotocol":<String_value>,
"snmpsecurityname":<String_value>,
"snmpprivprotocol":<String_value>,
"ns_ip_address_arr":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"snmpprivpassword":<String_value>,
"snmpversion":<String_value>,
"snmpauthpassword":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_snmp_config/

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_snmp_config:{
"snmpsecurityname":<String_value>,
"snmpauthprotocol":<String_value>,
"ns_ip_address":<String_value>,
"state":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"save_config":<Boolean_value>,
"trapdestination":<String_value>,
"snmpprivprotocol":<String_value>,
"ns_ip_address_arr":<String_value[]>,
"snmpprivpassword":<String_value>,
"snmpversion":<String_value>,
"snmpauthpassword":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_snmp_config":[{
"save_config":<Boolean_value>,
"trapdestination":<String_value>,
"snmpauthprotocol":<String_value>,
"snmpsecurityname":<String_value>,
"snmpprivprotocol":<String_value>,
"ns_ip_address_arr":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"snmpsecuritylevel":<String_value>,
"snmpcommunity":<String_value>,
"snmpprivpassword":<String_value>,
"snmpversion":<String_value>,
"snmpauthpassword":<String_value>}]}
```







