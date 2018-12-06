#ns_syslog_config



Configuration for NetScaler Syslog Config resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>informational</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable informational.</td></tr><tr><td>alert</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable alert.</td></tr><tr><td>none</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable none.</td></tr><tr><td>all</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable all.</td></tr><tr><td>facility</td><td>&lt;String></td><td>Read-write</td><td>Facility.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>Syslog Status.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Netscaler IP Address.</td></tr><tr><td>notice</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable notice.</td></tr><tr><td>destination_ip</td><td>&lt;String></td><td>Read-write</td><td>Syslog Destination IP Address.</td></tr><tr><td>critical</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable critical.</td></tr><tr><td>emergency</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable emergency.</td></tr><tr><td>warning</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable warning.</td></tr><tr><td>error</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable error.</td></tr><tr><td>debug</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable debug.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_syslog_config

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_syslog_config":[{
"informational":<Boolean_value>,
"alert":<Boolean_value>,
"none":<Boolean_value>,
"all":<Boolean_value>,
"facility":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"notice":<Boolean_value>,
"destination_ip":<String_value>,
"critical":<Boolean_value>,
"emergency":<Boolean_value>,
"warning":<Boolean_value>,
"error":<Boolean_value>,
"debug":<Boolean_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_syslog_config/ns_ip_address_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_syslog_config":[{
"informational":<Boolean_value>,
"alert":<Boolean_value>,
"none":<Boolean_value>,
"all":<Boolean_value>,
"facility":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"notice":<Boolean_value>,
"destination_ip":<String_value>,
"critical":<Boolean_value>,
"emergency":<Boolean_value>,
"warning":<Boolean_value>,
"error":<Boolean_value>,
"debug":<Boolean_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_syslog_config/ns_ip_address_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_syslog_config:{
"none":<Boolean_value>,
"all":<Boolean_value>,
"ns_ip_address":<String_value>,
"state":<String_value>,
"facility":<String_value>,
"emergency":<Boolean_value>,
"critical":<Boolean_value>,
"destination_ip":<String_value>,
"notice":<Boolean_value>,
"debug":<Boolean_value>,
"error":<Boolean_value>,
"alert":<Boolean_value>,
"informational":<Boolean_value>,
"warning":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_syslog_config":[{
"informational":<Boolean_value>,
"alert":<Boolean_value>,
"none":<Boolean_value>,
"all":<Boolean_value>,
"facility":<String_value>,
"state":<String_value>,
"ns_ip_address":<String_value>,
"notice":<Boolean_value>,
"destination_ip":<String_value>,
"critical":<Boolean_value>,
"emergency":<Boolean_value>,
"warning":<Boolean_value>,
"error":<Boolean_value>,
"debug":<Boolean_value>}]}
```







