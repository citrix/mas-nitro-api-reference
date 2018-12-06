#tenant



Configuration for Tenants resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>service_type</td><td>&lt;Double></td><td>Read-write</td><td>Type of service, Setting the bits for MAS, NGS, WAF.</td></tr><tr><td>dbrole_name</td><td>&lt;String></td><td>Read-write</td><td>Database Role Name for tenant.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>system_resource</td><td>&lt;tenant_system_resource></td><td>Read-write</td><td>Tenant System Resource.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of the Tenant.<br>Minimum length = 1<br>Maximum length = 512</td></tr><tr><td>schema_name</td><td>&lt;String></td><td>Read-write</td><td>Schema Name for tenant.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>company_info</td><td>&lt;tenant_company_info></td><td>Read-write</td><td>Tenant Company Information.</td></tr><tr><td>user_name</td><td>&lt;String></td><td>Read-write</td><td>User Name for tenant.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant ID of the parent Tenant..</td></tr><tr><td>access_to_parent</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable Shell access for non-nsroot User(s).</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>preauthtoken</td><td>&lt;String></td><td>Read-write</td><td>Preauth token for a tenant.<br>Minimum length = 1<br>Maximum length = 512</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the Tenants.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{tenant: {
<b>"user_name":<String_value></b>,
<b>"parent_id":<String_value></b>,
<b>"password":<String_value></b>,
"dbrole_name":<String_value>,
"service_type":<Double_value>,
"system_resource":<tenant_system_resource_value>,
"name":<String_value>,
"schema_name":<String_value>,
"company_info":<tenant_company_info_value>,
"access_to_parent":<Boolean_value>,
"preauthtoken":<String_value>,
"id":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant":[{
"service_type":<Double_value>,
"dbrole_name":<String_value>,
"system_resource":<tenant_system_resource_value>,
"name":<String_value>,
"schema_name":<String_value>,
"company_info":<tenant_company_info_value>,
"user_name":<String_value>,
"parent_id":<String_value>,
"access_to_parent":<Boolean_value>,
"password":<String_value>,
"preauthtoken":<String_value>,
"id":<String_value>,
"admin_tenant":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant":[{
"service_type":<Double_value>,
"dbrole_name":<String_value>,
"system_resource":<tenant_system_resource_value>,
"name":<String_value>,
"schema_name":<String_value>,
"company_info":<tenant_company_info_value>,
"user_name":<String_value>,
"parent_id":<String_value>,
"access_to_parent":<Boolean_value>,
"password":<String_value>,
"preauthtoken":<String_value>,
"id":<String_value>,
"admin_tenant":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant":[{
"service_type":<Double_value>,
"dbrole_name":<String_value>,
"system_resource":<tenant_system_resource_value>,
"name":<String_value>,
"schema_name":<String_value>,
"company_info":<tenant_company_info_value>,
"user_name":<String_value>,
"parent_id":<String_value>,
"access_to_parent":<Boolean_value>,
"password":<String_value>,
"preauthtoken":<String_value>,
"id":<String_value>,
"admin_tenant":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tenant/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{tenant:{
<b>"id":<String_value></b>,
"dbrole_name":<String_value>,
"service_type":<Double_value>,
"system_resource":<tenant_system_resource_value>,
"name":<String_value>,
"schema_name":<String_value>,
"company_info":<tenant_company_info_value>,
"parent_id":<String_value>,
"user_name":<String_value>,
"password":<String_value>,
"access_to_parent":<Boolean_value>,
"preauthtoken":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tenant":[{
"service_type":<Double_value>,
"dbrole_name":<String_value>,
"system_resource":<tenant_system_resource_value>,
"name":<String_value>,
"schema_name":<String_value>,
"company_info":<tenant_company_info_value>,
"user_name":<String_value>,
"parent_id":<String_value>,
"access_to_parent":<Boolean_value>,
"password":<String_value>,
"preauthtoken":<String_value>,
"id":<String_value>,
"admin_tenant":<String_value>}]}
```







