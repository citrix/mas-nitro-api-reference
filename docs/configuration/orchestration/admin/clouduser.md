#clouduser



Configuration for A cloud user resource represents a tenant in the cloud. Tenants are the unit of accounting: Resources (such as devices, network services, etc.) are always associated with tenants based on configured policies. resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>parent</td><td>&lt;String></td><td>Read-write</td><td>parent tenant ID - default: None.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-write</td><td>Status of the tenant - ACTIVE or DOWN.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of tenant..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>ID of the tenant.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Textual description of the tenant.</td></tr><tr><td>resources</td><td>&lt;resource></td><td>Read-only</td><td>Resources allocated to this tenant.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/clouduser?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{clouduser: {
"parent":<String_value>,
"status":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "clouduser":[{
"resources":<resource_value>,
"parent":<String_value>,
"status":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/clouduser/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/clouduser

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "clouduser":[{
"resources":<resource_value>,
"parent":<String_value>,
"status":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/clouduser/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "clouduser":[{
"resources":<resource_value>,
"parent":<String_value>,
"status":<String_value>,
"name":<String_value>,
"id":<String_value>,
"description":<String_value>}]}
```







