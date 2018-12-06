#system_settings



Configuration for System Settings resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>svm_ns_comm</td><td>&lt;String></td><td>Read-write</td><td>Communication with Instances.<br>Minimum length = 1<br>Maximum length = 10</td></tr><tr><td>session_timeout</td><td>&lt;Integer></td><td>Read-write</td><td>Session timeout for the system.</td></tr><tr><td>session_timeout_unit</td><td>&lt;String></td><td>Read-write</td><td>Session timeout unit for the system.</td></tr><tr><td>enable_nsrecover_login</td><td>&lt;Boolean></td><td>Read-write</td><td>This setting enalbes nsrecover login for SVM.</td></tr><tr><td>enable_session_timeout</td><td>&lt;Boolean></td><td>Read-write</td><td>Enables session timeout feature.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key.</td></tr><tr><td>enable_certificate_download</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable Certificate Download.</td></tr><tr><td>enable_apiproxy_credentials</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable API Proxy Credentials.</td></tr><tr><td>enable_shell_access</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable Shell access for non-nsroot User(s).</td></tr><tr><td>basicauth</td><td>&lt;Boolean></td><td>Read-write</td><td>Allow Basic Authentication Protocol.</td></tr><tr><td>secure_access_only</td><td>&lt;Boolean></td><td>Read-write</td><td>Secure Access only.</td></tr><tr><td>is_metering_enabled</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable Metering for NS VPX's on SDX.</td></tr><tr><td>port_model</td><td>&lt;Integer></td><td>Read-only</td><td>Port Model for BR instance.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/system_settings

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "system_settings":[{
"svm_ns_comm":<String_value>,
"session_timeout":<Integer_value>,
"session_timeout_unit":<String_value>,
"enable_nsrecover_login":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"port_model":<Integer_value>,
"id":<String_value>,
"ns_br_interface":<String_value>,
"enable_certificate_download":<Boolean_value>,
"init_status":<Integer_value>,
"enable_apiproxy_credentials":<Boolean_value>,
"ns_br_interface_2":<String_value>,
"enable_shell_access":<Boolean_value>,
"basicauth":<Boolean_value>,
"secure_access_only":<Boolean_value>,
"vm_auto_poweron":<Boolean_value>,
"is_metering_enabled":<Boolean_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>,
"reset":<Boolean_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/system_settings/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{system_settings:{
"session_timeout":<Integer_value>,
"session_timeout_unit":<String_value>,
"enable_session_timeout":<Boolean_value>,
"id":<String_value>,
"enable_shell_access":<Boolean_value>,
"basicauth":<Boolean_value>,
"secure_access_only":<Boolean_value>,
"svm_ns_comm":<String_value>,
"enable_nsrecover_login":<Boolean_value>,
"enable_certificate_download":<Boolean_value>,
"enable_apiproxy_credentials":<Boolean_value>,
"is_metering_enabled":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "system_settings":[{
"svm_ns_comm":<String_value>,
"session_timeout":<Integer_value>,
"session_timeout_unit":<String_value>,
"enable_nsrecover_login":<Boolean_value>,
"enable_session_timeout":<Boolean_value>,
"port_model":<Integer_value>,
"id":<String_value>,
"ns_br_interface":<String_value>,
"enable_certificate_download":<Boolean_value>,
"init_status":<Integer_value>,
"enable_apiproxy_credentials":<Boolean_value>,
"ns_br_interface_2":<String_value>,
"enable_shell_access":<Boolean_value>,
"basicauth":<Boolean_value>,
"secure_access_only":<Boolean_value>,
"vm_auto_poweron":<Boolean_value>,
"is_metering_enabled":<Boolean_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>,
"reset":<Boolean_value>}]}
```







