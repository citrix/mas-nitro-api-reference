#cc_profile



Configuration for Cloud Profile resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>client_secret</td><td>&lt;String></td><td>Read-write</td><td>Secret.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>client_id</td><td>&lt;String></td><td>Read-write</td><td>ID.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant Id of cloud profile.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the cloud profiles.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>Profile Name.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-only</td><td>Profile state.</td></tr><tr><td>email</td><td>&lt;String></td><td>Read-only</td><td>Email address of cloud profile holder.</td></tr><tr><td>customer_id</td><td>&lt;String></td><td>Read-only</td><td>Customer ID of the cloud profile holder.</td></tr><tr><td>is_set</td><td>&lt;Boolean></td><td>Read-only</td><td>True, if this profile is updated by user.</td></tr><tr><td>end_point</td><td>&lt;String></td><td>Read-only</td><td>End point of the service.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/cc_profile

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "cc_profile":[{
"name":<String_value>,
"client_secret":<String_value>,
"client_id":<String_value>,
"state":<String_value>,
"email":<String_value>,
"tenant_id":<String_value>,
"customer_id":<String_value>,
"is_set":<Boolean_value>,
"id":<String_value>,
"end_point":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/cc_profile/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "cc_profile":[{
"name":<String_value>,
"client_secret":<String_value>,
"client_id":<String_value>,
"state":<String_value>,
"email":<String_value>,
"tenant_id":<String_value>,
"customer_id":<String_value>,
"is_set":<Boolean_value>,
"id":<String_value>,
"end_point":<String_value>}]}
```







###update







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/cc_profile/id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{cc_profile:{
<b>"id":<String_value></b>,
"client_id":<String_value>,
"client_secret":<String_value>,
"tenant_id":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "cc_profile":[{
"name":<String_value>,
"client_secret":<String_value>,
"client_id":<String_value>,
"state":<String_value>,
"email":<String_value>,
"tenant_id":<String_value>,
"customer_id":<String_value>,
"is_set":<Boolean_value>,
"id":<String_value>,
"end_point":<String_value>}]}
```







