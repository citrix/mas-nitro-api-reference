#device_backup



Configuration for Device Backup resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>external_storage_info</td><td>&lt;backup_external_storage></td><td>Read-write</td><td>Information of the External storage for backup file.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device family..</td></tr><tr><td>image_filesize</td><td>&lt;Integer></td><td>Read-write</td><td>Image File Size.</td></tr><tr><td>last_updated_time</td><td>&lt;Integer></td><td>Read-write</td><td>Last Updated Time.</td></tr><tr><td>backup_filesize</td><td>&lt;Integer></td><td>Read-write</td><td>Backup file size.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all backed up files.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>Device IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>encrypted</td><td>&lt;Boolean></td><td>Read-write</td><td>Indicates if the backup files are encrypted.</td></tr><tr><td>backup_password</td><td>&lt;String></td><td>Read-write</td><td>Backup Password.</td></tr><tr><td>use_global_password</td><td>&lt;Boolean></td><td>Read-write</td><td>Global Password.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant ID.</td></tr><tr><td>device_name</td><td>&lt;String></td><td>Read-only</td><td>Device Hostname.</td></tr><tr><td>image_filename</td><td>&lt;String></td><td>Read-only</td><td>Name of the image file backed up.</td></tr><tr><td>backup_filename</td><td>&lt;String></td><td>Read-only</td><td>Name of the backed up file.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[DEVICEBACKUP](#deviceb)| [DELETE](#delete)| [GET (ALL)](#get-all)| [DEVICERESTORE](#devicere)| [UPLOAD](#u)| [DOWNLOAD](#dow)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###devicebackup







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_backup?action=devicebackup;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{device_backup: {
"external_storage_info":<backup_external_storage_value>,
"last_updated_time":<Integer_value>,
"id":<String_value>,
"device_family":<String_value>,
"backup_filesize":<Integer_value>,
"backup_password":<String_value>,
"image_filesize":<Integer_value>,
"use_global_password":<Boolean_value>,
"ip_address":<String_value>,
"encrypted":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_backup":[{
"external_storage_info":<backup_external_storage_value>,
"device_family":<String_value>,
"image_filesize":<Integer_value>,
"last_updated_time":<Integer_value>,
"backup_filesize":<Integer_value>,
"tenant_id":<String_value>,
"device_name":<String_value>,
"image_filename":<String_value>,
"backup_filename":<String_value>,
"id":<String_value>,
"ip_address":<String_value>,
"encrypted":<Boolean_value>,
"act_id":<String_value>,
"backup_password":<String_value>,
"use_global_password":<Boolean_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_backup/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_backup

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_backup":[{
"external_storage_info":<backup_external_storage_value>,
"device_family":<String_value>,
"image_filesize":<Integer_value>,
"last_updated_time":<Integer_value>,
"backup_filesize":<Integer_value>,
"tenant_id":<String_value>,
"device_name":<String_value>,
"image_filename":<String_value>,
"backup_filename":<String_value>,
"id":<String_value>,
"ip_address":<String_value>,
"encrypted":<Boolean_value>,
"act_id":<String_value>,
"backup_password":<String_value>,
"use_global_password":<Boolean_value>}]}
```







###devicerestore







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/device_backup?action=devicerestore;onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{device_backup: {
"external_storage_info":<backup_external_storage_value>,
"last_updated_time":<Integer_value>,
"id":<String_value>,
"device_family":<String_value>,
"backup_filesize":<Integer_value>,
"backup_password":<String_value>,
"image_filesize":<Integer_value>,
"use_global_password":<Boolean_value>,
"ip_address":<String_value>,
"encrypted":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "device_backup":[{
"external_storage_info":<backup_external_storage_value>,
"device_family":<String_value>,
"image_filesize":<Integer_value>,
"last_updated_time":<Integer_value>,
"backup_filesize":<Integer_value>,
"tenant_id":<String_value>,
"device_name":<String_value>,
"image_filename":<String_value>,
"backup_filename":<String_value>,
"id":<String_value>,
"ip_address":<String_value>,
"encrypted":<Boolean_value>,
"act_id":<String_value>,
"backup_password":<String_value>,
"use_global_password":<Boolean_value>}]}
```







###upload







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/upload/device_backup

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done }
```







###download







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/download/device_backup/id_value&lt;String&gt;

<b>HTTP Method:</b>null







