#ns_upgrade

Configuration for Upgrade NetScaler resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>scheduleTimesEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>device_groups</td><td>&lt;String[]></td><td>Read-write</td><td>Device Group Array on which for which job is run.</td></tr><tr><td>image_name</td><td>&lt;String></td><td>Read-write</td><td>image_name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>do_backup</td><td>&lt;Boolean></td><td>Read-write</td><td>True, if user wants to take backup before ns upgrade.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name.<br>Maximum length = 128</td></tr><tr><td>doc_file</td><td>&lt;String></td><td>Read-write</td><td>Documentation File Name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>ns_ip_address_arr</td><td>&lt;String[]></td><td>Read-write</td><td>List of NS IP Address.</td></tr><tr><td>scheduleId</td><td>&lt;String></td><td>Read-write</td><td>scheduleId is used to refer maintenaince schedule task.</td></tr><tr><td>mail_profiles</td><td>&lt;String></td><td>Read-write</td><td>Comma seperated list of Mail profiles.</td></tr><tr><td>ha_two_phase_upgrade</td><td>&lt;Boolean></td><td>Read-write</td><td>True, if user wants to upgarde ha in two phases or steps.</td></tr><tr><td>ha_node2_devices</td><td>&lt;String[]></td><td>Read-write</td><td>List of HA NS IP Address upgrade in second phase.</td></tr><tr><td>do_cleanup</td><td>&lt;Boolean></td><td>Read-write</td><td>True, if user wants to clean the image files once upgrade is completed successfully.</td></tr><tr><td>scheduleTimesEpoch2</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch for ha primary node (string representation of 11 digit numbers)..</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[UPGRADE](#up)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###upgrade



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_upgrade?action=upgrade;onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{ns_upgrade: {<b>"image_name":<String_value></b>,"do_cleanup":<Boolean_value>,"scheduleTimesEpoch":<String_value>,"device_groups":<String_value[]>,"doc_file":<String_value>,"name":<String_value>,"do_backup":<Boolean_value>,"ns_ip_address_arr":<String_value[]>,"mail_profiles":<String_value>,"scheduleId":<String_value>,"ha_two_phase_upgrade":<Boolean_value>,"ha_node2_devices":<String_value[]>,"scheduleTimesEpoch2":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_upgrade":[{"scheduleTimesEpoch":<String_value>,"device_groups":<String_value>,"mode":<Integer_value>,"image_name":<String_value>,"do_backup":<Boolean_value>,"name":<String_value>,"doc_file":<String_value>,"ns_ip_address_arr":<String_value>,"scheduleId":<String_value>,"mail_profiles":<String_value>,"act_id":<String_value>,"ha_two_phase_upgrade":<Boolean_value>,"ha_node2_devices":<String_value>,"do_cleanup":<Boolean_value>,"scheduleTimesEpoch2":<String_value>}]}```



