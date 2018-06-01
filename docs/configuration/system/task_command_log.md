#task_command_log

Configuration for Task Command Log resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>index</td><td>&lt;Integer></td><td>Read-write</td><td>Stores the order of the command..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the task command logs.</td></tr><tr><td>protocol</td><td>&lt;String></td><td>Read-only</td><td>Protocol.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Status.</td></tr><tr><td>starttime</td><td>&lt;Integer></td><td>Read-only</td><td>Start Time.</td></tr><tr><td>task_device_id</td><td>&lt;String></td><td>Read-only</td><td>Task Device ID.</td></tr><tr><td>endtime</td><td>&lt;Integer></td><td>Read-only</td><td>End Time.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-only</td><td>IP Address.</td></tr><tr><td>statusmessage</td><td>&lt;String></td><td>Read-only</td><td>Status Message.</td></tr><tr><td>command</td><td>&lt;String></td><td>Read-only</td><td>Command.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/task_command_log
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "task_command_log":[{"protocol":<String_value>,"status":<String_value>,"index":<Integer_value>,"starttime":<Integer_value>,"id":<String_value>,"task_device_id":<String_value>,"endtime":<Integer_value>,"ip_address":<String_value>,"statusmessage":<String_value>,"command":<String_value>}]}```



###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/task_command_log/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "task_command_log":[{"protocol":<String_value>,"status":<String_value>,"index":<Integer_value>,"starttime":<Integer_value>,"id":<String_value>,"task_device_id":<String_value>,"endtime":<Integer_value>,"ip_address":<String_value>,"statusmessage":<String_value>,"command":<String_value>}]}```



