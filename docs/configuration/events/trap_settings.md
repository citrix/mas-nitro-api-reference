#trap_settings



Configuration for trap severities resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>source</td><td>&lt;String></td><td>Read-write</td><td>Source.</td></tr><tr><td>default_severity</td><td>&lt;String></td><td>Read-write</td><td>default severity of trap.</td></tr><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Device Family.</td></tr><tr><td>oid</td><td>&lt;String></td><td>Read-write</td><td>Trap OID.</td></tr><tr><td>user_defined_severity</td><td>&lt;String></td><td>Read-write</td><td>user defined severity of trap.</td></tr><tr><td>trap_description</td><td>&lt;String></td><td>Read-write</td><td>Trap Description.</td></tr><tr><td>trap_category</td><td>&lt;String></td><td>Read-write</td><td>Trap Category.</td></tr><tr><td>is_suppress</td><td>&lt;Boolean></td><td>Read-write</td><td>if trap needs to be suppressed or not.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>source_array</td><td>&lt;String[]></td><td>Read-write</td><td>Source list.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/trap_settings

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "trap_settings":[{
"source":<String_value>,
"default_severity":<String_value>,
"device_family":<String_value>,
"oid":<String_value>,
"user_defined_severity":<String_value>,
"trap_description":<String_value>,
"trap_category":<String_value>,
"is_suppress":<Boolean_value>,
"id":<String_value>,
"source_array":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/trap_settings/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "trap_settings":[{
"source":<String_value>,
"default_severity":<String_value>,
"device_family":<String_value>,
"oid":<String_value>,
"user_defined_severity":<String_value>,
"trap_description":<String_value>,
"trap_category":<String_value>,
"is_suppress":<Boolean_value>,
"id":<String_value>,
"source_array":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/trap_settings/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{trap_settings:{
<b>"id":<String_value></b>,
"trap_description":<String_value>,
"is_suppress":<Boolean_value>,
"device_family":<String_value>,
"source_array":<String_value[]>,
"trap_category":<String_value>,
"source":<String_value>,
"default_severity":<String_value>,
"oid":<String_value>,
"user_defined_severity":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "trap_settings":[{
"source":<String_value>,
"default_severity":<String_value>,
"device_family":<String_value>,
"oid":<String_value>,
"user_defined_severity":<String_value>,
"trap_description":<String_value>,
"trap_category":<String_value>,
"is_suppress":<Boolean_value>,
"id":<String_value>,
"source_array":<String_value>}]}
```







