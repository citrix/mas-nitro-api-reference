#ns_pre_upgrade



Configuration for Pre Upgrade fro NetScaler resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>disk_space_error_details</td><td>&lt;String></td><td>Read-write</td><td>Disk space error for /var.</td></tr><tr><td>hardware_error_details</td><td>&lt;String></td><td>Read-write</td><td>Hardware error like HDD error details.</td></tr><tr><td>disk_space_error</td><td>&lt;String></td><td>Read-write</td><td>Disk space error for /var.</td></tr><tr><td>hardware_error</td><td>&lt;String></td><td>Read-write</td><td>Hardware error like HDD error.</td></tr><tr><td>user_custom_info</td><td>&lt;String></td><td>Read-write</td><td>User custom info.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address.</td></tr><tr><td>user_custom_info_details</td><td>&lt;String></td><td>Read-write</td><td>User custom info details.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[DELETE](#delete)| [GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_pre_upgrade/

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_pre_upgrade

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_pre_upgrade":[{
"disk_space_error_details":<String_value>,
"hardware_error_details":<String_value>,
"act_id":<String_value>,
"disk_space_error":<String_value>,
"hardware_error":<String_value>,
"user_custom_info":<String_value>,
"ip_address":<String_value>,
"user_custom_info_details":<String_value>}]}
```







