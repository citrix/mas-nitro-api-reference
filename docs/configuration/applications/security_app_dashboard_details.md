#security_app_dashboard_details

Configuration for Security App Dashboard Report table resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>violation_category</td><td>&lt;String></td><td>Read-write</td><td>violation Category..</td></tr><tr><td>app_threat_index</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>ns_city</td><td>&lt;String></td><td>Read-write</td><td>NetScaler Location city.</td></tr><tr><td>severity_type</td><td>&lt;String></td><td>Read-write</td><td>severity_type.<br>Maximum length = 255</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>app_category</td><td>&lt;String></td><td>Read-write</td><td>App Category.<br>Maximum length = 255</td></tr><tr><td>country_code</td><td>&lt;String></td><td>Read-write</td><td>country_code.<br>Maximum length = 255</td></tr><tr><td>violation_type</td><td>&lt;String></td><td>Read-write</td><td>Violation Type.</td></tr><tr><td>block_flags_prev</td><td>&lt;Double></td><td>Read-write</td><td>Block flag count.</td></tr><tr><td>safety_index</td><td>&lt;Double></td><td>Read-write</td><td>safety index..</td></tr><tr><td>app_safety_index_prev</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>appname</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>threat_index</td><td>&lt;Double></td><td>Read-write</td><td>threat_index.</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>city.</td></tr><tr><td>total_attacks_prev</td><td>&lt;Double></td><td>Read-write</td><td>Count of attacks in given sampled timeframe..</td></tr><tr><td>latitude</td><td>&lt;Double></td><td>Read-write</td><td>latitude.</td></tr><tr><td>ctnsappname</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>Netscaler IP Address..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>app_safety_index</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>country.<br>Maximum length = 255</td></tr><tr><td>longitude</td><td>&lt;Double></td><td>Read-write</td><td>longitude.</td></tr><tr><td>source_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Client ip address.<br>Maximum length = 255</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of NetScaler Instance.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Violation Type Description.</td></tr><tr><td>total_attacks</td><td>&lt;Double></td><td>Read-write</td><td>Count of this URL in given sampled timeframe..</td></tr><tr><td>device_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Device IP Address.<br>Maximum length = 255</td></tr><tr><td>attack_category</td><td>&lt;String></td><td>Read-write</td><td>Attack Category..</td></tr><tr><td>ns_latitude</td><td>&lt;Double></td><td>Read-write</td><td>NetScaler Location latitude.</td></tr><tr><td>exporter_id</td><td>&lt;String></td><td>Read-write</td><td>Exporter ID.<br>Maximum length = 255</td></tr><tr><td>vserver_name</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>ns_longitude</td><td>&lt;Double></td><td>Read-write</td><td>NetScaler Location longitude.</td></tr><tr><td>app_threat_index_prev</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>block_flags</td><td>&lt;Double></td><td>Read-write</td><td>Block flag count.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/security_app_dashboard_details
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "security_app_dashboard_details":[{"violation_category":<String_value>,"app_threat_index":<Double_value>,"ns_city":<String_value>,"severity_type":<String_value>,"__count":<Double_value>,"app_category":<String_value>,"country_code":<String_value>,"violation_type":<String_value>,"block_flags_prev":<Double_value>,"safety_index":<Double_value>,"app_safety_index_prev":<Double_value>,"appname":<String_value>,"threat_index":<Double_value>,"city":<String_value>,"total_attacks_prev":<Double_value>,"latitude":<Double_value>,"ctnsappname":<String_value>,"ip_address":<String_value>,"app_safety_index":<Double_value>,"country":<String_value>,"longitude":<Double_value>,"source_ip_address":<String_value>,"name":<String_value>,"rpt_sample_time":<Double_value>,"description":<String_value>,"total_attacks":<Double_value>,"device_ip_address":<String_value>,"attack_category":<String_value>,"ns_latitude":<Double_value>,"exporter_id":<String_value>,"vserver_name":<String_value>,"ns_longitude":<Double_value>,"app_threat_index_prev":<Double_value>,"block_flags":<Double_value>}]}```



