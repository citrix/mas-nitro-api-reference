#audit_log



Configuration for Audit Log resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant Id of the audit log.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the audit log entries.</td></tr><tr><td>command</td><td>&lt;String></td><td>Read-write</td><td>Command given for this action.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Status of this action whether accepted/rejected by system.</td></tr><tr><td>port</td><td>&lt;Integer></td><td>Read-only</td><td>Client port from where operation specified for this entry was performed.</td></tr><tr><td>message</td><td>&lt;String></td><td>Read-only</td><td>Message for this action.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-only</td><td>User Name, who performed operation specified for this entry.</td></tr><tr><td>client_type</td><td>&lt;String></td><td>Read-only</td><td>Client Type.</td></tr><tr><td>audittime</td><td>&lt;Integer></td><td>Read-only</td><td>Action Time on which operation specified for this entry was started.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-only</td><td>Client IP Address from where operation specified for this entry was performed.</td></tr><tr><td>resource_name</td><td>&lt;String></td><td>Read-only</td><td>Resource Name on which operation specified for this entry was performed.</td></tr><tr><td>operation</td><td>&lt;String></td><td>Read-only</td><td>Operation Type that is performed.</td></tr><tr><td>resource_type</td><td>&lt;String></td><td>Read-only</td><td>Resource Type on which operation specified for this entry was performed .</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/audit_log

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "audit_log":[{
"status":<String_value>,
"port":<Integer_value>,
"message":<String_value>,
"username":<String_value>,
"client_type":<String_value>,
"tenant_id":<String_value>,
"audittime":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"resource_name":<String_value>,
"operation":<String_value>,
"command":<String_value>,
"resource_type":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/audit_log/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "audit_log":[{
"status":<String_value>,
"port":<Integer_value>,
"message":<String_value>,
"username":<String_value>,
"client_type":<String_value>,
"tenant_id":<String_value>,
"audittime":<Integer_value>,
"id":<String_value>,
"ip_address":<String_value>,
"resource_name":<String_value>,
"operation":<String_value>,
"command":<String_value>,
"resource_type":<String_value>}]}
```







