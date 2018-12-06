#syslog_messages



Configuration for System Log Message resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>source</td><td>&lt;String></td><td>Read-write</td><td>Source IP Address.</td></tr><tr><td>event_type</td><td>&lt;String></td><td>Read-write</td><td>Event type.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-write</td><td>Message.</td></tr><tr><td>app_name</td><td>&lt;String></td><td>Read-write</td><td>Application Name.</td></tr><tr><td>system_time</td><td>&lt;String></td><td>Read-write</td><td>System Time in local timezone.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the system log entries.</td></tr><tr><td>instance_ip</td><td>&lt;String></td><td>Read-write</td><td>Instance IP Address.</td></tr><tr><td>severity</td><td>&lt;String></td><td>Read-write</td><td>Severity of the message.</td></tr><tr><td>module</td><td>&lt;String></td><td>Read-write</td><td>Module name.</td></tr><tr><td>system_gmt_time</td><td>&lt;Integer></td><td>Read-only</td><td>System Time in GMT timezone.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_messages

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_messages":[{
"source":<String_value>,
"event_type":<String_value>,
"system_gmt_time":<Integer_value>,
"message":<String_value>,
"app_name":<String_value>,
"system_time":<String_value>,
"id":<String_value>,
"instance_ip":<String_value>,
"severity":<String_value>,
"module":<String_value>}]}
```







