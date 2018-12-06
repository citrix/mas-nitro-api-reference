#syslog_generic



Configuration for Syslog generic table resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the syslog generic record..</td></tr><tr><td>source</td><td>&lt;String></td><td>Read-only</td><td>source..</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-only</td><td>Device family.</td></tr><tr><td>event_id</td><td>&lt;Double></td><td>Read-only</td><td>;ltTODO&gt;.</td></tr><tr><td>system_name</td><td>&lt;String></td><td>Read-only</td><td>Device System Name.</td></tr><tr><td>full_message</td><td>&lt;String></td><td>Read-only</td><td>Syslog original Message..</td></tr><tr><td>isparsed</td><td>&lt;Boolean></td><td>Read-only</td><td>Whethersyslog message is parsed successfully or not.</td></tr><tr><td>ttime</td><td>&lt;Double></td><td>Read-only</td><td>ttime.</td></tr><tr><td>device_type</td><td>&lt;String></td><td>Read-only</td><td>Device Type.</td></tr><tr><td>host_name</td><td>&lt;String></td><td>Read-only</td><td>Assign hostname to managed device, if this is not provided, name will be set as host name .</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Type Name..</td></tr><tr><td>syslog_msg</td><td>&lt;String></td><td>Read-only</td><td>Syslog original Message..</td></tr><tr><td>severity</td><td>&lt;String></td><td>Read-only</td><td>severity.</td></tr><tr><td>module</td><td>&lt;String></td><td>Read-only</td><td>Module Name..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/syslog_generic

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "syslog_generic":[{
"source":<String_value>,
"device_family":<String_value>,
"event_id":<Double_value>,
"system_name":<String_value>,
"full_message":<String_value>,
"isparsed":<Boolean_value>,
"ttime":<Double_value>,
"device_type":<String_value>,
"host_name":<String_value>,
"id":<String_value>,
"type":<String_value>,
"syslog_msg":<String_value>,
"severity":<String_value>,
"module":<String_value>}]}
```







