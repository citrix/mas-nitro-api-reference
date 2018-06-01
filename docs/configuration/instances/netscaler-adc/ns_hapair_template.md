#ns_hapair_template

Configuration for NS HA Pair Configure Template resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>nssecondary_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Secondary HA Node NSIP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>backplane</td><td>&lt;String></td><td>Read-write</td><td>Backplane Interface.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>clusterid</td><td>&lt;Integer></td><td>Read-write</td><td>Cluster Id.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>secondary_nodeid</td><td>&lt;Integer></td><td>Read-write</td><td>Secondary Node ID.<br>Maximum value =</td></tr><tr><td>execute_sequentially</td><td>&lt;Boolean></td><td>Read-write</td><td>True if configuration template is to be applied to devices sequentially.</td></tr><tr><td>nsprimary_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Primary HA Node NSIP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>clip</td><td>&lt;String></td><td>Read-write</td><td>Cluster IPAddress.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>primary_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Primary HA Node IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>configCoordinator</td><td>&lt;String></td><td>Read-write</td><td>Node to be designated as Config Coordinator - primary or secondary.</td></tr><tr><td>scheduleTimesEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>secondary_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Secondary HA Node IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name.<br>Maximum length = 128</td></tr><tr><td>primary_nodeid</td><td>&lt;Integer></td><td>Read-write</td><td>Prmiary Node ID.<br>Maximum value =</td></tr><tr><td>on_error</td><td>&lt;String></td><td>Read-write</td><td>Behaviour on encountering error while applying configuration template on a device: CONTINUE|EXIT.<br>Minimum length = 1<br>Maximum length = 16</td></tr><tr><td>inc_enabled</td><td>&lt;Boolean></td><td>Read-write</td><td>Turn on INC mode on self node.</td></tr><tr><td>scheduleId</td><td>&lt;String></td><td>Read-write</td><td>scheduleId is used to refer maintenaince schedule task.</td></tr><tr><td>mail_profiles</td><td>&lt;String></td><td>Read-write</td><td>Comma seperated list of Mail profiles.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_hapair_template
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_hapair_template":[{"nssecondary_ip_address":<String_value>,"backplane":<String_value>,"clusterid":<Integer_value>,"secondary_nodeid":<Integer_value>,"execute_sequentially":<Boolean_value>,"nsprimary_ip_address":<String_value>,"act_id":<String_value>,"clip":<String_value>,"primary_ip_address":<String_value>,"configCoordinator":<String_value>,"scheduleTimesEpoch":<String_value>,"secondary_ip_address":<String_value>,"name":<String_value>,"primary_nodeid":<Integer_value>,"on_error":<String_value>,"inc_enabled":<Boolean_value>,"scheduleId":<String_value>,"mail_profiles":<String_value>,"sync_operation":<Boolean_value>}]}```



