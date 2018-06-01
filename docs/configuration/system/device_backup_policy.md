#device_backup_policy

Configuration for Device Backup Policy resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>external_storage_info</td><td>&lt;backup_external_storage></td><td>Read-write</td><td>Information of the External storage for backup file.</td></tr><tr><td>backup_on_cfg_sav_trap</td><td>&lt;Boolean></td><td>Read-write</td><td>Backup On recieving NetscalerConfigSave trap.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device family whose devices need to be backed up..</td></tr><tr><td>backup_password</td><td>&lt;String></td><td>Read-write</td><td>Password for backup file encryption.</td></tr><tr><td>encrypt_backup_file</td><td>&lt;Boolean></td><td>Read-write</td><td>Encrypts backup files.</td></tr><tr><td>enable_scheduled_backups</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable Scheduled Backup (default is enabled).</td></tr><tr><td>enable_external_transfer</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable transfer of device backup files to external server.</td></tr><tr><td>polling_interval</td><td>&lt;Integer></td><td>Read-write</td><td>Frequency of device backup in hours.</td></tr><tr><td>backup_times</td><td>&lt;String></td><td>Read-write</td><td>Comma Separated string of backup times to be scheduled..</td></tr><tr><td>number_of_backups</td><td>&lt;Integer></td><td>Read-write</td><td>Number of backup files maintained per device.<br>Minimum value = 1</td></tr><tr><td>is_interval_based</td><td>&lt;Boolean></td><td>Read-write</td><td>Parameter to decide whether backup setting is interval based or time based.</td></tr><tr><td>enable_geodb_backups</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable GeoDB Backup from NetScaler (default is disabled).</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[DO_POLL](#do)| [GET]()| [UPDATE](#u)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###do_poll



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_backup_policy?action=do_poll;onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{device_backup_policy: {<b>"number_of_backups":<Integer_value></b>,<b>"is_interval_based":<Boolean_value></b>,"external_storage_info":<backup_external_storage_value>,"enable_scheduled_backups":<Boolean_value>,"device_family":<String_value>,"encrypt_backup_file":<Boolean_value>,"enable_external_transfer":<Boolean_value>,"backup_times":<String_value>,"backup_on_cfg_sav_trap":<Boolean_value>,"backup_password":<String_value>,"polling_interval":<Integer_value>,"enable_geodb_backups":<Boolean_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_backup_policy":[{"external_storage_info":<backup_external_storage_value>,"backup_on_cfg_sav_trap":<Boolean_value>,"device_family":<String_value>,"backup_password":<String_value>,"encrypt_backup_file":<Boolean_value>,"enable_scheduled_backups":<Boolean_value>,"enable_external_transfer":<Boolean_value>,"polling_interval":<Integer_value>,"backup_times":<String_value>,"number_of_backups":<Integer_value>,"is_interval_based":<Boolean_value>,"enable_geodb_backups":<Boolean_value>}]}```



###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_backup_policy
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_backup_policy":[{"external_storage_info":<backup_external_storage_value>,"backup_on_cfg_sav_trap":<Boolean_value>,"device_family":<String_value>,"backup_password":<String_value>,"encrypt_backup_file":<Boolean_value>,"enable_scheduled_backups":<Boolean_value>,"enable_external_transfer":<Boolean_value>,"polling_interval":<Integer_value>,"backup_times":<String_value>,"number_of_backups":<Integer_value>,"is_interval_based":<Boolean_value>,"enable_geodb_backups":<Boolean_value>}]}```



###update



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_backup_policy/
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{device_backup_policy:{<b>"number_of_backups":<Integer_value></b>,<b>"is_interval_based":<Boolean_value></b>,"external_storage_info":<backup_external_storage_value>,"enable_scheduled_backups":<Boolean_value>,"device_family":<String_value>,"encrypt_backup_file":<Boolean_value>,"enable_external_transfer":<Boolean_value>,"backup_times":<String_value>,"backup_on_cfg_sav_trap":<Boolean_value>,"backup_password":<String_value>,"polling_interval":<Integer_value>,"enable_geodb_backups":<Boolean_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_backup_policy":[{"external_storage_info":<backup_external_storage_value>,"backup_on_cfg_sav_trap":<Boolean_value>,"device_family":<String_value>,"backup_password":<String_value>,"encrypt_backup_file":<Boolean_value>,"enable_scheduled_backups":<Boolean_value>,"enable_external_transfer":<Boolean_value>,"polling_interval":<Integer_value>,"backup_times":<String_value>,"number_of_backups":<Integer_value>,"is_interval_based":<Boolean_value>,"enable_geodb_backups":<Boolean_value>}]}```



