#device_group

Configuration for Device Group resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>static_device_list</td><td>&lt;String></td><td>Read-write</td><td>Devices in the group.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device Family.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>lock_acquiring_device</td><td>&lt;String></td><td>Read-write</td><td>Upgrade Lock acquiring device.<br>Maximum length = 255</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Device Group Name.<br>Maximum length = 255</td></tr><tr><td>duration</td><td>&lt;Integer></td><td>Read-write</td><td>Duration of Maintenance window for groups of category upgrade.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>maintenance_window_start</td><td>&lt;String></td><td>Read-write</td><td>Maintenance window start time for groups of category upgrade.<br>Maximum length = 255</td></tr><tr><td>criteria_type</td><td>&lt;String></td><td>Read-write</td><td>Device Group Criteria.<br>Maximum length = 255</td></tr><tr><td>upgrade_version</td><td>&lt;String></td><td>Read-write</td><td>New Available upgrade version for devices.<br>Maximum length = 255</td></tr><tr><td>criteria_condn</td><td>&lt;String></td><td>Read-write</td><td>Tenant.<br>Maximum length = 255</td></tr><tr><td>upgrade_lock</td><td>&lt;Boolean></td><td>Read-write</td><td>Lock to be acquired before upgrading device group.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for agent registered with NMX Cloud..</td></tr><tr><td>category</td><td>&lt;String></td><td>Read-write</td><td>Device group category. Will be default/upgrade..<br>Maximum length = 255</td></tr><tr><td>disable_upgrade</td><td>&lt;Boolean></td><td>Read-write</td><td>Setting to disable agent upgrades.</td></tr><tr><td>lock_acquire_time</td><td>&lt;String></td><td>Read-write</td><td>Upgrade Lock acquiring time.<br>Maximum length = 255</td></tr><tr><td>criteria_value</td><td>&lt;String></td><td>Read-write</td><td>Criteria Value.<br>Maximum length = 255</td></tr><tr><td>static_device_list_arr</td><td>&lt;String[]></td><td>Read-write</td><td>Static Device List.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [GET]()| [UPDATE](#u)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_group?onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{device_group: {<b>"duration":<Integer_value></b>,"static_device_list":<String_value>,"lock_acquiring_device":<String_value>,"criteria_condn":<String_value>,"category":<String_value>,"id":<String_value>,"criteria_value":<String_value>,"device_family":<String_value>,"name":<String_value>,"upgrade_lock":<Boolean_value>,"disable_upgrade":<Boolean_value>,"lock_acquire_time":<String_value>,"upgrade_version":<String_value>,"static_device_list_arr":<String_value[]>,"criteria_type":<String_value>,"maintenance_window_start":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_group":[{"static_device_list":<String_value>,"device_family":<String_value>,"lock_acquiring_device":<String_value>,"name":<String_value>,"duration":<Integer_value>,"maintenance_window_start":<String_value>,"criteria_type":<String_value>,"upgrade_version":<String_value>,"criteria_condn":<String_value>,"upgrade_lock":<Boolean_value>,"tenant_id":<String_value>,"id":<String_value>,"category":<String_value>,"disable_upgrade":<Boolean_value>,"lock_acquire_time":<String_value>,"criteria_value":<String_value>,"static_device_list_arr":<String_value>}]}```



###delete



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_group/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }```



###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_group
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_group":[{"static_device_list":<String_value>,"device_family":<String_value>,"lock_acquiring_device":<String_value>,"name":<String_value>,"duration":<Integer_value>,"maintenance_window_start":<String_value>,"criteria_type":<String_value>,"upgrade_version":<String_value>,"criteria_condn":<String_value>,"upgrade_lock":<Boolean_value>,"tenant_id":<String_value>,"id":<String_value>,"category":<String_value>,"disable_upgrade":<Boolean_value>,"lock_acquire_time":<String_value>,"criteria_value":<String_value>,"static_device_list_arr":<String_value>}]}```



###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_group/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_group":[{"static_device_list":<String_value>,"device_family":<String_value>,"lock_acquiring_device":<String_value>,"name":<String_value>,"duration":<Integer_value>,"maintenance_window_start":<String_value>,"criteria_type":<String_value>,"upgrade_version":<String_value>,"criteria_condn":<String_value>,"upgrade_lock":<Boolean_value>,"tenant_id":<String_value>,"id":<String_value>,"category":<String_value>,"disable_upgrade":<Boolean_value>,"lock_acquire_time":<String_value>,"criteria_value":<String_value>,"static_device_list_arr":<String_value>}]}```



###update



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_group/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{device_group:{<b>"duration":<Integer_value></b>,"static_device_list":<String_value>,"lock_acquiring_device":<String_value>,"criteria_condn":<String_value>,"category":<String_value>,"id":<String_value>,"criteria_value":<String_value>,"device_family":<String_value>,"name":<String_value>,"upgrade_lock":<Boolean_value>,"disable_upgrade":<Boolean_value>,"lock_acquire_time":<String_value>,"upgrade_version":<String_value>,"static_device_list_arr":<String_value[]>,"criteria_type":<String_value>,"maintenance_window_start":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_group":[{"static_device_list":<String_value>,"device_family":<String_value>,"lock_acquiring_device":<String_value>,"name":<String_value>,"duration":<Integer_value>,"maintenance_window_start":<String_value>,"criteria_type":<String_value>,"upgrade_version":<String_value>,"criteria_condn":<String_value>,"upgrade_lock":<Boolean_value>,"tenant_id":<String_value>,"id":<String_value>,"category":<String_value>,"disable_upgrade":<Boolean_value>,"lock_acquire_time":<String_value>,"criteria_value":<String_value>,"static_device_list_arr":<String_value>}]}```



