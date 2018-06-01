#si_geo_location

Configuration for AF Geo Threat Data Report table resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>severity_type</td><td>&lt;String></td><td>Read-write</td><td>severity_type.<br>Maximum length = 255</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>violation_type</td><td>&lt;String></td><td>Read-write</td><td>violation_type.<br>Maximum length = 2048</td></tr><tr><td>country_code</td><td>&lt;String></td><td>Read-write</td><td>country_code.<br>Maximum length = 255</td></tr><tr><td>violation_action</td><td>&lt;String></td><td>Read-write</td><td>violation_action.<br>Maximum length = 255</td></tr><tr><td>signature_category</td><td>&lt;String></td><td>Read-write</td><td>signature_category.<br>Maximum length = 255</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>city.<br>Maximum length = 255</td></tr><tr><td>threat_index</td><td>&lt;Double></td><td>Read-write</td><td>threat_index.</td></tr><tr><td>latitude</td><td>&lt;Double></td><td>Read-write</td><td>latitude.</td></tr><tr><td>violation_name</td><td>&lt;String></td><td>Read-write</td><td>violation_name.<br>Maximum length = 255</td></tr><tr><td>violation_location</td><td>&lt;String></td><td>Read-write</td><td>violation_location.<br>Maximum length = 255</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is Security check violation name.<br>Maximum length = 255</td></tr><tr><td>severity</td><td>&lt;String></td><td>Read-write</td><td>severity.<br>Maximum length = 255</td></tr><tr><td>http_method</td><td>&lt;String></td><td>Read-write</td><td>http_method.<br>Maximum length = 50</td></tr><tr><td>violation_value</td><td>&lt;String></td><td>Read-write</td><td>violation_value.<br>Maximum length = 255</td></tr><tr><td>not_blocked_flags</td><td>&lt;Double></td><td>Read-write</td><td>total attacks..</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>country.<br>Maximum length = 255</td></tr><tr><td>longitude</td><td>&lt;Double></td><td>Read-write</td><td>longitude.</td></tr><tr><td>source_ip_address</td><td>&lt;String></td><td>Read-write</td><td>source_ip_address.<br>Maximum length = 255</td></tr><tr><td>attack_time</td><td>&lt;String></td><td>Read-write</td><td>attack_time.<br>Maximum length = 255</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>violation_threat_index</td><td>&lt;String></td><td>Read-write</td><td>violation_threat_index.<br>Maximum length = 2048</td></tr><tr><td>total_attacks</td><td>&lt;Double></td><td>Read-write</td><td>total attacks..</td></tr><tr><td>attack_category</td><td>&lt;String></td><td>Read-write</td><td>attack_category.<br>Maximum length = 255</td></tr><tr><td>http_req_url</td><td>&lt;String></td><td>Read-write</td><td>http_req_url.<br>Maximum length = 2048</td></tr><tr><td>transformed_flags</td><td>&lt;Double></td><td>Read-write</td><td>transformed_flags..</td></tr><tr><td>block_flags</td><td>&lt;Double></td><td>Read-write</td><td>block_flags..</td></tr><tr><td>si_app_unit_name</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/si_geo_location
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "si_geo_location":[{"severity_type":<String_value>,"__count":<Double_value>,"violation_type":<String_value>,"country_code":<String_value>,"violation_action":<String_value>,"signature_category":<String_value>,"city":<String_value>,"threat_index":<Double_value>,"latitude":<Double_value>,"violation_name":<String_value>,"violation_location":<String_value>,"id":<String_value>,"severity":<String_value>,"http_method":<String_value>,"violation_value":<String_value>,"not_blocked_flags":<Double_value>,"country":<String_value>,"longitude":<Double_value>,"source_ip_address":<String_value>,"attack_time":<String_value>,"name":<String_value>,"violation_threat_index":<String_value>,"total_attacks":<Double_value>,"attack_category":<String_value>,"http_req_url":<String_value>,"si_device_ip_address":<String_value>,"transformed_flags":<Double_value>,"block_flags":<Double_value>,"si_app_unit_name":<String_value>}]}```



