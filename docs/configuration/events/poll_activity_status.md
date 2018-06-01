#poll_activity_status

Configuration for Activity Status resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>instance_level_progress</td><td>&lt;Integer></td><td>Read-write</td><td>Instance level Polling Progress Percentage.<br>Maximum value =</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-write</td><td>Status.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-write</td><td>Message.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>total_instances</td><td>&lt;Integer></td><td>Read-write</td><td>Total number of devices to be polled.</td></tr><tr><td>timestamp</td><td>&lt;Double></td><td>Read-write</td><td>timestamp in seconds.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the task logs.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr><tr><td>module</td><td>&lt;String></td><td>Read-only</td><td>Module name in which the Polling is done.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/poll_activity_status
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "poll_activity_status":[{"instance_level_progress":<Integer_value>,"status":<String_value>,"message":<String_value>,"ns_ip_address":<String_value>,"total_instances":<Integer_value>,"act_id":<String_value>,"timestamp":<Double_value>,"id":<String_value>,"module":<String_value>}]}```



###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/poll_activity_status/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "poll_activity_status":[{"instance_level_progress":<Integer_value>,"status":<String_value>,"message":<String_value>,"ns_ip_address":<String_value>,"total_instances":<Integer_value>,"act_id":<String_value>,"timestamp":<Double_value>,"id":<String_value>,"module":<String_value>}]}```



