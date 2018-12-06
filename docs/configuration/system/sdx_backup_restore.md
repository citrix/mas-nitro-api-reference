#sdx_backup_restore



Configuration for Backup resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ip_address_list</td><td>&lt;String[]></td><td>Read-write</td><td>List of VM IP Address.<br>Minimum length = 1<br>Maximum length = 1024</td></tr><tr><td>reset_type</td><td>&lt;Integer></td><td>Read-write</td><td>Reset Type [0: Reset (Without Network Configuration), 1: Reset (With Network Configuration), 2: Appliance Reset, 3: Appliance Restore, 4: Instance Restore, 5: Backup ].</td></tr><tr><td>file_name</td><td>&lt;String></td><td>Read-write</td><td>File Name.<br>Minimum length = 1<br>Maximum length = 256</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>Name of VM device.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-only</td><td>IP Address for this VM device.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-only</td><td>Type of device, (br | ns).</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[FACTORYRESET](#factory)| [GET](#get)| [RESTORE](#re)| [BACKUP](#b)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###factoryreset







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sdx_backup_restore?action=factoryreset;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{sdx_backup_restore: {
"file_name":<String_value>,
"reset_type":<Integer_value>,
"ip_address_list":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sdx_backup_restore":[{
"restore_type":<Integer_value>,
"ip_address_list":<String_value>,
"name":<String_value>,
"reset_type":<Integer_value>,
"sync_operation":<Boolean_value>,
"file_name":<String_value>,
"act_id":<String_value>,
"ip_address":<String_value>,
"type":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sdx_backup_restore

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sdx_backup_restore":[{
"restore_type":<Integer_value>,
"ip_address_list":<String_value>,
"name":<String_value>,
"reset_type":<Integer_value>,
"sync_operation":<Boolean_value>,
"file_name":<String_value>,
"act_id":<String_value>,
"ip_address":<String_value>,
"type":<String_value>}]}
```







###restore







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sdx_backup_restore?action=restore;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{sdx_backup_restore: {
"file_name":<String_value>,
"reset_type":<Integer_value>,
"ip_address_list":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sdx_backup_restore":[{
"restore_type":<Integer_value>,
"ip_address_list":<String_value>,
"name":<String_value>,
"reset_type":<Integer_value>,
"sync_operation":<Boolean_value>,
"file_name":<String_value>,
"act_id":<String_value>,
"ip_address":<String_value>,
"type":<String_value>}]}
```







###backup







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sdx_backup_restore?action=backup;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{sdx_backup_restore: {
"file_name":<String_value>,
"reset_type":<Integer_value>,
"ip_address_list":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sdx_backup_restore":[{
"restore_type":<Integer_value>,
"ip_address_list":<String_value>,
"name":<String_value>,
"reset_type":<Integer_value>,
"sync_operation":<Boolean_value>,
"file_name":<String_value>,
"act_id":<String_value>,
"ip_address":<String_value>,
"type":<String_value>}]}
```







