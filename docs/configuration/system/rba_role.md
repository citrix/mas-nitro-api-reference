#rba_role



Configuration for RBA Role resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant Id of the RBA roles.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Role Name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the RBA roles.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Description of Role.<br>Minimum length = 1<br>Maximum length = 1024</td></tr><tr><td>resourcegroups</td><td>&lt;String[]></td><td>Read-write</td><td>Resourcegroups attached to this role..</td></tr><tr><td>groups</td><td>&lt;String[]></td><td>Read-write</td><td>Groups to which this role is assigned.</td></tr><tr><td>policies</td><td>&lt;String[]></td><td>Read-write</td><td>Policies attached to this role..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_role?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{rba_role: {
<b>"name":<String_value></b>,
"groups":<String_value[]>,
"id":<String_value>,
"description":<String_value>,
"policies":<String_value[]>,
"tenant_id":<String_value>,
"resourcegroups":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_role":[{
"is_default":<Boolean_value>,
"tenant_id":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>,
"tenant_name":<String_value>,
"resourcegroups":<String_value>,
"groups":<String_value>,
"policies":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_role/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_role

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_role":[{
"is_default":<Boolean_value>,
"tenant_id":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>,
"tenant_name":<String_value>,
"resourcegroups":<String_value>,
"groups":<String_value>,
"policies":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_role/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_role":[{
"is_default":<Boolean_value>,
"tenant_id":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>,
"tenant_name":<String_value>,
"resourcegroups":<String_value>,
"groups":<String_value>,
"policies":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_role/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{rba_role:{
<b>"id":<String_value></b>,
"groups":<String_value[]>,
"name":<String_value>,
"description":<String_value>,
"policies":<String_value[]>,
"tenant_id":<String_value>,
"resourcegroups":<String_value[]>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_role":[{
"is_default":<Boolean_value>,
"tenant_id":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>,
"tenant_name":<String_value>,
"resourcegroups":<String_value>,
"groups":<String_value>,
"policies":<String_value>}]}
```







