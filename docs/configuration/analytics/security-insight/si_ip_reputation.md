#si_ip_reputation

Configuration for AF IP Reputation Report resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>source_ip_address</td><td>&lt;String></td><td>Read-write</td><td>source_ip_address.<br>Maximum length = 255</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>violation_type</td><td>&lt;String></td><td>Read-write</td><td>Violation Type.<br>Maximum length = 255</td></tr><tr><td>iprep_category</td><td>&lt;String></td><td>Read-write</td><td>Category of the IPREP.<br>Maximum length = 255</td></tr><tr><td>violation_action</td><td>&lt;String></td><td>Read-write</td><td>Violation Action.<br>Maximum length = 255</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>iprep_reputation_score</td><td>&lt;Double></td><td>Read-write</td><td>Reputation Score of IP.</td></tr><tr><td>total_attacks</td><td>&lt;Double></td><td>Read-write</td><td>total attacks..</td></tr><tr><td>attack_category</td><td>&lt;String></td><td>Read-write</td><td>Attack Category.<br>Maximum length = 255</td></tr><tr><td>iprep_severity</td><td>&lt;String></td><td>Read-write</td><td>Severity.<br>Maximum length = 255</td></tr><tr><td>iprep_attack_time</td><td>&lt;Double></td><td>Read-write</td><td>Time of Attack.</td></tr><tr><td>iprep_http_method</td><td>&lt;String></td><td>Read-write</td><td>HTTP Req method.<br>Maximum length = 255</td></tr><tr><td>iprep_app_threat_index</td><td>&lt;Double></td><td>Read-write</td><td>App Threat Index.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/si_ip_reputation
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "si_ip_reputation":[{"source_ip_address":<String_value>,"__count":<Double_value>,"violation_type":<String_value>,"iprep_category":<String_value>,"violation_action":<String_value>,"name":<String_value>,"rpt_sample_time":<Double_value>,"iprep_reputation_score":<Double_value>,"total_attacks":<Double_value>,"attack_category":<String_value>,"si_device_ip_address":<String_value>,"iprep_severity":<String_value>,"iprep_attack_time":<Double_value>,"iprep_http_method":<String_value>,"iprep_app_threat_index":<Double_value>}]}```



