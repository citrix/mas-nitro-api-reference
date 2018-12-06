#rba_module_client_data



Configuration for RBA Module Client Data resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>submodules</td><td>&lt;rba_submodule_client_data[]></td><td>Read-write</td><td>RBA submodule client data.</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>serial_id</td><td>&lt;Integer></td><td>Read-write</td><td>Sequence number.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>operation</td><td>&lt;rba_operation_client_data[]></td><td>Read-write</td><td>RBA operations client data.</td></tr><tr><td>child_node</td><td>&lt;String></td><td>Read-only</td><td>This property is for internal use.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-only</td><td>module name.</td></tr><tr><td>ui_component</td><td>&lt;Boolean></td><td>Read-only</td><td>This property shows, its a UI component.</td></tr><tr><td>display_name</td><td>&lt;String></td><td>Read-only</td><td>module display name.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_module_client_data

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_module_client_data":[{
"child_node":<String_value>,
"parent_name":<String_value>,
"name":<String_value>,
"submodules":[{
"child_node":<String_value>,
"parent_name":<String_value>,
"name":<String_value>,
"ui_component":<Boolean_value>,
"display_name":<String_value>,
"parent_id":<String_value>,
"serial_id":<Integer_value>,
"childmodules":[{
"child_node":<String_value>,
"parent_name":<String_value>,
"name":<String_value>,
"ui_component":<Boolean_value>,
"display_name":<String_value>,
"parent_id":<String_value>,
"serial_id":<Integer_value>,
"id":<String_value>,
"operation":[{
"parent_name":<String_value>,
"display_name":<String_value>,
"parent_id":<String_value>,
"operation_name":<String_value>,
"serial_id":<Integer_value>,
"id":<String_value>,
"type":<String_value>,
"dependent_resources":<String_value>,
"resource_type":<String_value>}]}],
"id":<String_value>,
"operation":[{
"parent_name":<String_value>,
"display_name":<String_value>,
"parent_id":<String_value>,
"operation_name":<String_value>,
"serial_id":<Integer_value>,
"id":<String_value>,
"type":<String_value>,
"dependent_resources":<String_value>,
"resource_type":<String_value>}]}],
"ui_component":<Boolean_value>,
"display_name":<String_value>,
"parent_id":<String_value>,
"serial_id":<Integer_value>,
"id":<String_value>,
"operation":[{
"parent_name":<String_value>,
"display_name":<String_value>,
"parent_id":<String_value>,
"operation_name":<String_value>,
"serial_id":<Integer_value>,
"id":<String_value>,
"type":<String_value>,
"dependent_resources":<String_value>,
"resource_type":<String_value>}]}]}
```







