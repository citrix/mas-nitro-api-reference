#configuration_template

Configuration for Configuration Template resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>device_family</td><td>&lt;String></td><td>Read-write</td><td>Family of Devices for which config template is defined..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>commands</td><td>&lt;config_command[]></td><td>Read-write</td><td>Array of commands part of the configuration template.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of configuration template.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>variables</td><td>&lt;config_variable[]></td><td>Read-write</td><td>Array of variables used in commands of the configuration template.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Description of configuration template.<br>Minimum length = 1<br>Maximum length = 1024</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant Id.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the configuration templates.</td></tr><tr><td>category</td><td>&lt;String></td><td>Read-write</td><td>Category of configuration template.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>is_inbuilt</td><td>&lt;Boolean></td><td>Read-only</td><td>true, if this template is in built.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[ADD]()| [DELETE](#d)| [GET (ALL)](#get-)| [MODIFY](#m)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###add



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/configuration_template?onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{configuration_template: {"parent_id":<String_value>,"category":<String_value>,"id":<String_value>,"parent_name":<String_value>,"device_family":<String_value>,"name":<String_value>,"description":<String_value>,"commands":[{"protocol":<String_value>,"nitro_method":<String_value>,"parent_id":<String_value>,"timeout":<Integer_value>,"id":<String_value>,"nitro_resource":<String_value>,"command":<String_value>,"parent_name":<String_value>,"nitro_payload":<String_value>,"index":<Integer_value>}],"variables":[{<b>"name":<String_value></b>,"parent_id":<String_value>,"required":<Boolean_value>,"default_value":<String_value>,"id":<String_value>,"values_enum":<String_value[]>,"values_enum_db":<String_value>,"parent_name":<String_value>,"description":<String_value>,"display_name":<String_value>,"type":<String_value>}],"tenant_id":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "configuration_template":[{"device_family":<String_value>,"parent_name":<String_value>,"commands":[{"protocol":<String_value>,"index":<Integer_value>,"parent_name":<String_value>,"timeout":<Integer_value>,"nitro_payload":<String_value>,"nitro_resource":<String_value>,"id":<String_value>,"nitro_method":<String_value>,"command":<String_value>,"parent_id":<String_value>}],"name":<String_value>,"variables":[{"parent_name":<String_value>,"name":<String_value>,"display_name":<String_value>,"description":<String_value>,"parent_id":<String_value>,"required":<Boolean_value>,"default_value":<String_value>,"id":<String_value>,"type":<String_value>,"values_enum_db":<String_value>,"values_enum":<String_value>}],"description":<String_value>,"parent_id":<String_value>,"is_visible":<Boolean_value>,"tenant_id":<String_value>,"id":<String_value>,"is_inbuilt":<Boolean_value>,"category":<String_value>}]}```



###delete



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/configuration_template/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }```



###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/configuration_template
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "configuration_template":[{"device_family":<String_value>,"parent_name":<String_value>,"commands":[{"protocol":<String_value>,"index":<Integer_value>,"parent_name":<String_value>,"timeout":<Integer_value>,"nitro_payload":<String_value>,"nitro_resource":<String_value>,"id":<String_value>,"nitro_method":<String_value>,"command":<String_value>,"parent_id":<String_value>}],"name":<String_value>,"variables":[{"parent_name":<String_value>,"name":<String_value>,"display_name":<String_value>,"description":<String_value>,"parent_id":<String_value>,"required":<Boolean_value>,"default_value":<String_value>,"id":<String_value>,"type":<String_value>,"values_enum_db":<String_value>,"values_enum":<String_value>}],"description":<String_value>,"parent_id":<String_value>,"is_visible":<Boolean_value>,"tenant_id":<String_value>,"id":<String_value>,"is_inbuilt":<Boolean_value>,"category":<String_value>}]}```



###modify



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/configuration_template/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{configuration_template:{<b>"id":<String_value></b>,"parent_id":<String_value>,"category":<String_value>,"parent_name":<String_value>,"device_family":<String_value>,"name":<String_value>,"description":<String_value>,"commands":[{"protocol":<String_value>,"nitro_method":<String_value>,"parent_id":<String_value>,"timeout":<Integer_value>,"id":<String_value>,"nitro_resource":<String_value>,"command":<String_value>,"parent_name":<String_value>,"nitro_payload":<String_value>,"index":<Integer_value>}],"variables":[{<b>"name":<String_value></b>,"parent_id":<String_value>,"required":<Boolean_value>,"default_value":<String_value>,"id":<String_value>,"values_enum":<String_value[]>,"values_enum_db":<String_value>,"parent_name":<String_value>,"description":<String_value>,"display_name":<String_value>,"type":<String_value>}],"tenant_id":<String_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "configuration_template":[{"device_family":<String_value>,"parent_name":<String_value>,"commands":[{"protocol":<String_value>,"index":<Integer_value>,"parent_name":<String_value>,"timeout":<Integer_value>,"nitro_payload":<String_value>,"nitro_resource":<String_value>,"id":<String_value>,"nitro_method":<String_value>,"command":<String_value>,"parent_id":<String_value>}],"name":<String_value>,"variables":[{"parent_name":<String_value>,"name":<String_value>,"display_name":<String_value>,"description":<String_value>,"parent_id":<String_value>,"required":<Boolean_value>,"default_value":<String_value>,"id":<String_value>,"type":<String_value>,"values_enum_db":<String_value>,"values_enum":<String_value>}],"description":<String_value>,"parent_id":<String_value>,"is_visible":<Boolean_value>,"tenant_id":<String_value>,"id":<String_value>,"is_inbuilt":<Boolean_value>,"category":<String_value>}]}```



