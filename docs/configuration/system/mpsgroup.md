#mpsgroup



Configuration for System Groups resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>allow_application_only</td><td>&lt;Boolean></td><td>Read-write</td><td>Checks if only application centic page is needed.</td></tr><tr><td>session_timeout</td><td>&lt;Integer></td><td>Read-write</td><td>Session timeout for the Group.</td></tr><tr><td>permission</td><td>&lt;String></td><td>Read-write</td><td>Permission for the group (admin/read-only).<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Group Name.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>session_timeout_unit</td><td>&lt;String></td><td>Read-write</td><td>Session timeout unit for the Group.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Description of Group.<br>Minimum length = 1<br>Maximum length = 1024</td></tr><tr><td>assign_all_apps</td><td>&lt;Boolean></td><td>Read-write</td><td>Assign All Applications (YES|NO).</td></tr><tr><td>enable_session_timeout</td><td>&lt;Boolean></td><td>Read-write</td><td>Enables session timeout for group.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Id of the tenant.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>assign_all_devices</td><td>&lt;Boolean></td><td>Read-write</td><td>Assign All Instances (YES|NO).</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the system groups.</td></tr><tr><td>role</td><td>&lt;String></td><td>Read-write</td><td>Role (admin|nonadmin).</td></tr><tr><td>roles</td><td>&lt;String[]></td><td>Read-write</td><td>Roles assigned to the group.</td></tr><tr><td>application_names_without_regex</td><td>&lt;String[]></td><td>Read-write</td><td>selected application names that are part of this group.</td></tr><tr><td>standalone_instances_id</td><td>&lt;String[]></td><td>Read-write</td><td>Stand alone instances belong to this groupp.</td></tr><tr><td>users</td><td>&lt;String[]></td><td>Read-write</td><td>Users belong to the group.</td></tr><tr><td>application_names</td><td>&lt;String[]></td><td>Read-write</td><td>All Application names that are part of this group.This includes selected appnames as well as applications which are result of defined regex.</td></tr><tr><td>application_names_with_regex</td><td>&lt;String[]></td><td>Read-write</td><td>Application names defined with regex that are part of this group.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpsgroup?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{mpsgroup: {
<b>"permission":<String_value></b>,
<b>"name":<String_value></b>,
"session_timeout":<Integer_value>,
"session_timeout_unit":<String_value>,
"assign_all_apps":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"id":<String_value>,
"application_names_without_regex":<String_value[]>,
"roles":<String_value[]>,
"allow_application_only":<Boolean_value>,
"description":<String_value>,
"application_names":<String_value[]>,
"application_names_with_regex":<String_value[]>,
"role":<String_value>,
"standalone_instances_id":<String_value[]>,
"users":<String_value[]>,
"tenant_id":<String_value>,
"assign_all_devices":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mpsgroup":[{
"allow_application_only":<Boolean_value>,
"session_timeout":<Integer_value>,
"permission":<String_value>,
"name":<String_value>,
"session_timeout_unit":<String_value>,
"description":<String_value>,
"assign_all_apps":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"authscope_props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>
"propvalues":<String_value>}],
"tenant_id":<String_value>,
"assign_all_devices":<Boolean_value>,
"id":<String_value>,
"role":<String_value>,
"roles":<String_value>,
"application_names_without_regex":<String_value>,
"tenant_name":<String_value>,
"standalone_instances_id":<String_value>,
"users":<String_value>,
"application_names":<String_value>,
"application_list":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"application_names_with_regex":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpsgroup/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpsgroup

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mpsgroup":[{
"allow_application_only":<Boolean_value>,
"session_timeout":<Integer_value>,
"permission":<String_value>,
"name":<String_value>,
"session_timeout_unit":<String_value>,
"description":<String_value>,
"assign_all_apps":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"authscope_props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>
"propvalues":<String_value>}],
"tenant_id":<String_value>,
"assign_all_devices":<Boolean_value>,
"id":<String_value>,
"role":<String_value>,
"roles":<String_value>,
"application_names_without_regex":<String_value>,
"tenant_name":<String_value>,
"standalone_instances_id":<String_value>,
"users":<String_value>,
"application_names":<String_value>,
"application_list":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"application_names_with_regex":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpsgroup/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mpsgroup":[{
"allow_application_only":<Boolean_value>,
"session_timeout":<Integer_value>,
"permission":<String_value>,
"name":<String_value>,
"session_timeout_unit":<String_value>,
"description":<String_value>,
"assign_all_apps":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"authscope_props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>
"propvalues":<String_value>}],
"tenant_id":<String_value>,
"assign_all_devices":<Boolean_value>,
"id":<String_value>,
"role":<String_value>,
"roles":<String_value>,
"application_names_without_regex":<String_value>,
"tenant_name":<String_value>,
"standalone_instances_id":<String_value>,
"users":<String_value>,
"application_names":<String_value>,
"application_list":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"application_names_with_regex":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mpsgroup/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{mpsgroup:{
<b>"id":<String_value></b>,
"session_timeout":<Integer_value>,
"session_timeout_unit":<String_value>,
"assign_all_apps":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"application_names_without_regex":<String_value[]>,
"roles":<String_value[]>,
"allow_application_only":<Boolean_value>,
"name":<String_value>,
"permission":<String_value>,
"description":<String_value>,
"application_names":<String_value[]>,
"application_names_with_regex":<String_value[]>,
"role":<String_value>,
"standalone_instances_id":<String_value[]>,
"users":<String_value[]>,
"tenant_id":<String_value>,
"assign_all_devices":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mpsgroup":[{
"allow_application_only":<Boolean_value>,
"session_timeout":<Integer_value>,
"permission":<String_value>,
"name":<String_value>,
"session_timeout_unit":<String_value>,
"description":<String_value>,
"assign_all_apps":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"authscope_props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>
"propvalues":<String_value>}],
"tenant_id":<String_value>,
"assign_all_devices":<Boolean_value>,
"id":<String_value>,
"role":<String_value>,
"roles":<String_value>,
"application_names_without_regex":<String_value>,
"tenant_name":<String_value>,
"standalone_instances_id":<String_value>,
"users":<String_value>,
"application_names":<String_value>,
"application_list":[{
"parent_name":<String_value>,
"app_state":<String_value>,
"parent_id":<String_value>,
"device_ip_address":<String_value>,
"app_protocol":<String_value>,
"appname":<String_value>,
"app_ip_address":<String_value>,
"entity_id":<String_value>,
"app_type":<String_value>,
"id":<String_value>,
"config_path":<String_value>}],
"application_names_with_regex":<String_value>}]}
```







