#variable_values

Configuration for Variable Values required for config template execution resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>value</td><td>&lt;String></td><td>Read-write</td><td>Value of the Variable to be used for all device ips/groups.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Variable name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>display_name</td><td>&lt;String></td><td>Read-write</td><td>Display name of configuration variable.<br>Minimum length = 1<br>Maximum length = 1024</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Description of configuration variable.<br>Minimum length = 1<br>Maximum length = 1024</td></tr><tr><td>device_values</td><td>&lt;device_values_map[]></td><td>Read-write</td><td>Values of variables used in commands of the configuration template for individual devices.</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>default_value</td><td>&lt;String></td><td>Read-write</td><td>Default Value of configuration variable.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>type</td><td>&lt;String></td><td>Read-write</td><td>Type of Variable.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>values_enum_db</td><td>&lt;String></td><td>Read-write</td><td>Comma seperated list of possible values of variable.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/variable_values
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "variable_values":[{"device_values_mapping":<String_value>,"parent_name":<String_value>,"value":<String_value>,"name":<String_value>,"display_name":<String_value>,"description":<String_value>,"device_values":[{"parent_name":<String_value>,"value":<String_value>,"id":<String_value>,"device_group":<String_value>,"device":<String_value>,"parent_id":<String_value>}],"parent_id":<String_value>,"default_value":<String_value>,"id":<String_value>,"type":<String_value>,"values_enum_db":<String_value>}]}```



