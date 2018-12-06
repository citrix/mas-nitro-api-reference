#managed_app



Configuration for Managed Application resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>app_networking_data</td><td>&lt;String></td><td>Read-write</td><td>app networking blob that can be used by placement logic.</td></tr><tr><td>is_app_placed</td><td>&lt;Boolean></td><td>Read-write</td><td>1 if app is placed on some NS, else 0..</td></tr><tr><td>lb_role</td><td>&lt;String></td><td>Read-write</td><td>Application is applied only on the devices with the same Lb role.</td></tr><tr><td>container_manager</td><td>&lt;String></td><td>Read-write</td><td>Container orchestration system.</td></tr><tr><td>app_id</td><td>&lt;String></td><td>Read-write</td><td>Id for the managed application.</td></tr><tr><td>app_netfuncs_config</td><td>&lt;network_function_config[]></td><td>Read-write</td><td>Network function related config for the application.</td></tr><tr><td>networking_manager</td><td>&lt;String></td><td>Read-write</td><td>System used to setup the network.</td></tr><tr><td>app_dns</td><td>&lt;String></td><td>Read-write</td><td>Doman name service for Application.</td></tr><tr><td>appname</td><td>&lt;String></td><td>Read-write</td><td>Name of the Application.</td></tr><tr><td>dns_manager</td><td>&lt;String></td><td>Read-write</td><td>Domain Name Service manager.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Dummy Id needed for input get requests.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [MODIFY](#m)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/managed_app?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{managed_app: {
"is_app_placed":<Boolean_value>,
"container_manager":<String_value>,
"networking_manager":<String_value>,
"app_netfuncs_config":[{
"parent_id":<String_value>,
"id":<String_value>,
"parent_name":<String_value>,
"type":<String_value>,
"netfunc_params":<network_function_param_value>}],
"id":<String_value>,
"app_networking_data":<String_value>,
"app_id":<String_value>,
"app_dns":<String_value>,
"appname":<String_value>,
"dns_manager":<String_value>,
"lb_role":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "managed_app":[{
"app_networking_data":<String_value>,
"is_app_placed":<Boolean_value>,
"lb_role":<String_value>,
"container_manager":<String_value>,
"app_id":<String_value>,
"app_netfuncs_config":[{
"parent_name":<String_value>,
"netfunc_params":<network_function_param_value>,
"type":<String_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"networking_manager":<String_value>,
"app_dns":<String_value>,
"appname":<String_value>,
"dns_manager":<String_value>,
"id":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/managed_app/app_id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/managed_app

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "managed_app":[{
"app_networking_data":<String_value>,
"is_app_placed":<Boolean_value>,
"lb_role":<String_value>,
"container_manager":<String_value>,
"app_id":<String_value>,
"app_netfuncs_config":[{
"parent_name":<String_value>,
"netfunc_params":<network_function_param_value>,
"type":<String_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"networking_manager":<String_value>,
"app_dns":<String_value>,
"appname":<String_value>,
"dns_manager":<String_value>,
"id":<String_value>}]}
```







###modify







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/managed_app/app_id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{managed_app:{
<b>"app_id":<String_value></b>,
"is_app_placed":<Boolean_value>,
"container_manager":<String_value>,
"networking_manager":<String_value>,
"app_netfuncs_config":[{
"parent_id":<String_value>,
"id":<String_value>,
"parent_name":<String_value>,
"type":<String_value>,
"netfunc_params":<network_function_param_value>}],
"id":<String_value>,
"app_networking_data":<String_value>,
"app_dns":<String_value>,
"appname":<String_value>,
"dns_manager":<String_value>,
"lb_role":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "managed_app":[{
"app_networking_data":<String_value>,
"is_app_placed":<Boolean_value>,
"lb_role":<String_value>,
"container_manager":<String_value>,
"app_id":<String_value>,
"app_netfuncs_config":[{
"parent_name":<String_value>,
"netfunc_params":<network_function_param_value>,
"type":<String_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"networking_manager":<String_value>,
"app_dns":<String_value>,
"appname":<String_value>,
"dns_manager":<String_value>,
"id":<String_value>}]}
```







