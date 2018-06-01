#maintenance_job

Configuration for Maintenance Job resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>scheduleTimesEpoch</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Family of Devices for which config job was executed.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>tasklog_id</td><td>&lt;String></td><td>Read-write</td><td>Task Log Id of the Config Job.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of maintenance job.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>task_name</td><td>&lt;String></td><td>Read-write</td><td>task name..</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>mail_profiles</td><td>&lt;String></td><td>Read-write</td><td>Comma seperated list of Mail profiles.</td></tr><tr><td>resource</td><td>&lt;String></td><td>Read-write</td><td>resource name..</td></tr><tr><td>action</td><td>&lt;String></td><td>Read-write</td><td>Schedule time epoch (string representation of 11 digit numbers)..</td></tr><tr><td>resource_object</td><td>&lt;String></td><td>Read-write</td><td>Resource object payload..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the maintenance jobs.</td></tr><tr><td>attached_maintenance_job</td><td>&lt;String></td><td>Read-write</td><td>Attached maintenance job.</td></tr><tr><td>scheduleTime</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated times of the day(DD:HH:MM) on which Configuration Template is scheduled.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Status of Config Job.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-only</td><td>Name of user who created maintenance job.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id of the Config Jobs.</td></tr><tr><td>timestamp</td><td>&lt;Integer></td><td>Read-only</td><td>Time of Creation of Maintenance Job.</td></tr><tr><td>devices_count</td><td>&lt;Integer></td><td>Read-only</td><td>Number of Devices on which commands executed.</td></tr><tr><td>devices_completed_count</td><td>&lt;Integer></td><td>Read-only</td><td>Devices Completed Count.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [MODIFY](#m)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/maintenance_job?onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{maintenance_job: {"task_name":<String_value>,"attached_maintenance_job":<String_value>,"parent_id":<String_value>,"resource_object":<String_value>,"id":<String_value>,"scheduleTimesEpoch":<String_value>,"device_family":<String_value>,"tasklog_id":<String_value>,"name":<String_value>,"mail_profiles":<String_value>,"scheduleTime":<String_value>,"resource":<String_value>,"action":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "maintenance_job":[{"scheduleTimesEpoch":<String_value>,"device_family":<String_value>,"status":<String_value>,"tasklog_id":<String_value>,"name":<String_value>,"task_name":<String_value>,"parent_id":<String_value>,"username":<String_value>,"mail_profiles":<String_value>,"resource":<String_value>,"tenant_id":<String_value>,"timestamp":<Integer_value>,"action":<String_value>,"resource_object":<String_value>,"id":<String_value>,"devices_count":<Integer_value>,"attached_maintenance_job":<String_value>,"scheduleTime":<String_value>,"devices_completed_count":<Integer_value>}]}```



###delete



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/maintenance_job/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }```



###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/maintenance_job
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "maintenance_job":[{"scheduleTimesEpoch":<String_value>,"device_family":<String_value>,"status":<String_value>,"tasklog_id":<String_value>,"name":<String_value>,"task_name":<String_value>,"parent_id":<String_value>,"username":<String_value>,"mail_profiles":<String_value>,"resource":<String_value>,"tenant_id":<String_value>,"timestamp":<Integer_value>,"action":<String_value>,"resource_object":<String_value>,"id":<String_value>,"devices_count":<Integer_value>,"attached_maintenance_job":<String_value>,"scheduleTime":<String_value>,"devices_completed_count":<Integer_value>}]}```



###modify



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/maintenance_job/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{maintenance_job:{<b>"id":<String_value></b>,"task_name":<String_value>,"attached_maintenance_job":<String_value>,"parent_id":<String_value>,"resource_object":<String_value>,"scheduleTimesEpoch":<String_value>,"device_family":<String_value>,"tasklog_id":<String_value>,"name":<String_value>,"mail_profiles":<String_value>,"scheduleTime":<String_value>,"resource":<String_value>,"action":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "maintenance_job":[{"scheduleTimesEpoch":<String_value>,"device_family":<String_value>,"status":<String_value>,"tasklog_id":<String_value>,"name":<String_value>,"task_name":<String_value>,"parent_id":<String_value>,"username":<String_value>,"mail_profiles":<String_value>,"resource":<String_value>,"tenant_id":<String_value>,"timestamp":<Integer_value>,"action":<String_value>,"resource_object":<String_value>,"id":<String_value>,"devices_count":<Integer_value>,"attached_maintenance_job":<String_value>,"scheduleTime":<String_value>,"devices_completed_count":<Integer_value>}]}```



