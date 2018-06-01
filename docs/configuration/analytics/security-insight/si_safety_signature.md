#si_safety_signature

Configuration for AF Safety Data Report table resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sig_learn</td><td>&lt;Double></td><td>Read-write</td><td>sig_learn..</td></tr><tr><td>sig_rule_id</td><td>&lt;Double></td><td>Read-write</td><td>Signature Rule Id.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>sig_none</td><td>&lt;Double></td><td>Read-write</td><td>sig_none..</td></tr><tr><td>configuration</td><td>&lt;String></td><td>Read-write</td><td>Profile Security configuration.<br>Maximum length = 255</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is safety profile.<br>Maximum length = 255</td></tr><tr><td>sig_block_count</td><td>&lt;Double></td><td>Read-write</td><td>sig_block_count..</td></tr><tr><td>sig_rule_category</td><td>&lt;String></td><td>Read-write</td><td>Profile sig_rule_category.<br>Maximum length = 2550</td></tr><tr><td>sig_sig_name</td><td>&lt;String></td><td>Read-write</td><td>Profile signature name.<br>Maximum length = 2550</td></tr><tr><td>sig_block</td><td>&lt;Double></td><td>Read-write</td><td>sig_block..</td></tr><tr><td>sig_stat_count</td><td>&lt;Double></td><td>Read-write</td><td>sig_stat_count..</td></tr><tr><td>sig_rule_logstring</td><td>&lt;String></td><td>Read-write</td><td>Profile sig_rule_logstring.<br>Maximum length = 2550</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Profile Name.<br>Maximum length = 255</td></tr><tr><td>sig_log</td><td>&lt;Double></td><td>Read-write</td><td>sig_log..</td></tr><tr><td>profile_sig_disable_count</td><td>&lt;Double></td><td>Read-write</td><td>profile_sig_disable_count..</td></tr><tr><td>profile_not_block_count</td><td>&lt;Double></td><td>Read-write</td><td>profile_not_block_count..</td></tr><tr><td>sig_log_count</td><td>&lt;Double></td><td>Read-write</td><td>sig_log_count..</td></tr><tr><td>sig_stat</td><td>&lt;Double></td><td>Read-write</td><td>sig_stat..</td></tr><tr><td>si_app_unit_name</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>sig_safety_index</td><td>&lt;Double></td><td>Read-write</td><td>sig_safety_index..</td></tr><tr><td>profile_safety_index</td><td>&lt;Double></td><td>Read-write</td><td>profile_safety_index..</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/si_safety_signature
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "si_safety_signature":[{"sig_learn":<Double_value>,"sig_rule_id":<Double_value>,"__count":<Double_value>,"sig_none":<Double_value>,"configuration":<String_value>,"id":<String_value>,"sig_block_count":<Double_value>,"sig_rule_category":<String_value>,"sig_sig_name":<String_value>,"sig_block":<Double_value>,"sig_stat_count":<Double_value>,"sig_rule_logstring":<String_value>,"name":<String_value>,"sig_log":<Double_value>,"profile_sig_disable_count":<Double_value>,"profile_not_block_count":<Double_value>,"si_device_ip_address":<String_value>,"sig_log_count":<Double_value>,"sig_stat":<Double_value>,"si_app_unit_name":<String_value>,"sig_safety_index":<Double_value>,"profile_safety_index":<Double_value>}]}```



