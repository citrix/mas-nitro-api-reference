#snmp_trap



Configuration for SNMP Trap Destinations resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>community</td><td>&lt;String></td><td>Read-write</td><td>Community Name.<br>Maximum length = 32</td></tr><tr><td>version</td><td>&lt;String></td><td>Read-write</td><td>SNMP version.<br>Maximum length = 2</td></tr><tr><td>dest_server</td><td>&lt;String></td><td>Read-write</td><td>Trap Destination Server Address.</td></tr><tr><td>dest_port</td><td>&lt;Integer></td><td>Read-write</td><td>Destination Port.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>user_name</td><td>&lt;String[]></td><td>Read-write</td><td>Name of SNMP Trap User.<br>Minimum length = 1<br>Maximum length = 32</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_trap?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{snmp_trap: {
<b>"dest_server":<String_value></b>,
"version":<String_value>,
"user_name":<String_value[]>,
"community":<String_value>,
"dest_port":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_trap":[{
"community":<String_value>,
"version":<String_value>,
"dest_server":<String_value>,
"dest_port":<Integer_value>,
"user_name":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_trap/dest_server_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_trap

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_trap":[{
"community":<String_value>,
"version":<String_value>,
"dest_server":<String_value>,
"dest_port":<Integer_value>,
"user_name":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_trap/dest_server_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_trap":[{
"community":<String_value>,
"version":<String_value>,
"dest_server":<String_value>,
"dest_port":<Integer_value>,
"user_name":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/snmp_trap/dest_server_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{snmp_trap:{
<b>"dest_server":<String_value></b>,
"version":<String_value>,
"user_name":<String_value[]>,
"community":<String_value>,
"dest_port":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "snmp_trap":[{
"community":<String_value>,
"version":<String_value>,
"dest_server":<String_value>,
"dest_port":<Integer_value>,
"user_name":<String_value>}]}
```







