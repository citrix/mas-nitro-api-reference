#si_safety_system_security

Configuration for AF Safety System Security Data Report table resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>sub_group</td><td>&lt;String></td><td>Read-write</td><td>System Sub Group Name.<br>Maximum length = 255</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Profile Security Check Type Name.<br>Maximum length = 255</td></tr><tr><td>num_configs</td><td>&lt;Double></td><td>Read-write</td><td>num_configs..</td></tr><tr><td>recommended_action</td><td>&lt;String></td><td>Read-write</td><td>System recommended_action.<br>Maximum length = 500</td></tr><tr><td>system_safety_index</td><td>&lt;Double></td><td>Read-write</td><td>system_safety_index..</td></tr><tr><td>is_complaint</td><td>&lt;String></td><td>Read-write</td><td>System compliant.<br>Maximum length = 255</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is safety profile.<br>Maximum length = 255</td></tr><tr><td>si_app_unit_name</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>profile_safety_index</td><td>&lt;Double></td><td>Read-write</td><td>profile_safety_index..</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/si_safety_system_security
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "si_safety_system_security":[{"__count":<Double_value>,"sub_group":<String_value>,"name":<String_value>,"num_configs":<Double_value>,"recommended_action":<String_value>,"system_safety_index":<Double_value>,"si_device_ip_address":<String_value>,"is_complaint":<String_value>,"id":<String_value>,"si_app_unit_name":<String_value>,"profile_safety_index":<Double_value>}]}```



