#syslog_server



Configuration for Syslog Server resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>log_level_all</td><td>&lt;Boolean></td><td>Read-write</td><td>Send logs of all levels to this syslog server.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Syslog server name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>log_level_warning</td><td>&lt;Boolean></td><td>Read-write</td><td>Send logs of level warning to this syslog server.</td></tr><tr><td>log_level_error</td><td>&lt;Boolean></td><td>Read-write</td><td>Send logs of level error to this syslog server.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-write</td><td>Syslog server port.<br>Maximum value =</td></tr><tr><td>log_level_info</td><td>&lt;Boolean></td><td>Read-write</td><td>Send logs of level info to this syslog server.</td></tr><tr><td>log_level_critical</td><td>&lt;Boolean></td><td>Read-write</td><td>Send logs of level critical to this syslog server.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>Syslog server IP address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>log_level_none</td><td>&lt;Boolean></td><td>Read-write</td><td>Send no logs to this syslog server.</td></tr><tr><td>log_levels</td><td>&lt;String></td><td>Read-only</td><td>Set of all log levels at which messages are sent to this syslog server.</td></tr><tr><td>address_type</td><td>&lt;Integer></td><td>Read-only</td><td>Configuration Type. Values: 0: IPv4, 1: IPv6.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [MODIFY](#m)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_server?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{syslog_server: {
<b>"name":<String_value></b>,
<b>"port":<Integer_value></b>,
<b>"ip_address":<String_value></b>,
"log_level_all":<Boolean_value>,
"log_level_info":<Boolean_value>,
"log_level_critical":<Boolean_value>,
"log_level_none":<Boolean_value>,
"log_level_error":<Boolean_value>,
"log_level_warning":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_server":[{
"log_level_all":<Boolean_value>,
"log_level_alert":<Boolean_value>,
"name":<String_value>,
"log_level_debug":<Boolean_value>,
"log_level_warning":<Boolean_value>,
"log_level_error":<Boolean_value>,
"port":<Integer_value>,
"log_levels":<String_value>,
"log_level_info":<Boolean_value>,
"log_level_notice":<Boolean_value>,
"log_level_critical":<Boolean_value>,
"ip_address":<String_value>,
"log_level_none":<Boolean_value>,
"address_type":<Integer_value>,
"log_level_emergency":<Boolean_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_server/name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_server

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_server":[{
"log_level_all":<Boolean_value>,
"log_level_alert":<Boolean_value>,
"name":<String_value>,
"log_level_debug":<Boolean_value>,
"log_level_warning":<Boolean_value>,
"log_level_error":<Boolean_value>,
"port":<Integer_value>,
"log_levels":<String_value>,
"log_level_info":<Boolean_value>,
"log_level_notice":<Boolean_value>,
"log_level_critical":<Boolean_value>,
"ip_address":<String_value>,
"log_level_none":<Boolean_value>,
"address_type":<Integer_value>,
"log_level_emergency":<Boolean_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_server/name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_server":[{
"log_level_all":<Boolean_value>,
"log_level_alert":<Boolean_value>,
"name":<String_value>,
"log_level_debug":<Boolean_value>,
"log_level_warning":<Boolean_value>,
"log_level_error":<Boolean_value>,
"port":<Integer_value>,
"log_levels":<String_value>,
"log_level_info":<Boolean_value>,
"log_level_notice":<Boolean_value>,
"log_level_critical":<Boolean_value>,
"ip_address":<String_value>,
"log_level_none":<Boolean_value>,
"address_type":<Integer_value>,
"log_level_emergency":<Boolean_value>}]}
```







###modify







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_server/name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{syslog_server:{
"log_level_all":<Boolean_value>,
"name":<String_value>,
"log_level_error":<Boolean_value>,
"log_level_warning":<Boolean_value>,
"port":<Integer_value>,
"log_level_info":<Boolean_value>,
"log_level_critical":<Boolean_value>,
"log_level_none":<Boolean_value>,
"ip_address":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_server":[{
"log_level_all":<Boolean_value>,
"log_level_alert":<Boolean_value>,
"name":<String_value>,
"log_level_debug":<Boolean_value>,
"log_level_warning":<Boolean_value>,
"log_level_error":<Boolean_value>,
"port":<Integer_value>,
"log_levels":<String_value>,
"log_level_info":<Boolean_value>,
"log_level_notice":<Boolean_value>,
"log_level_critical":<Boolean_value>,
"ip_address":<String_value>,
"log_level_none":<Boolean_value>,
"address_type":<Integer_value>,
"log_level_emergency":<Boolean_value>}]}
```







