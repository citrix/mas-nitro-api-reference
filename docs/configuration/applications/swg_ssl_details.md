#swg_ssl_details

Configuration for swg_ssl_details resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>ssli_executed_action</td><td>&lt;String></td><td>Read-write</td><td>SSL Executed Action..<br>Maximum length = 255</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>total_not_attempted_prev</td><td>&lt;Double></td><td>Read-write</td><td>total_not_attempted_prev.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>total_not_intercepted_prev</td><td>&lt;Double></td><td>Read-write</td><td>total_not_intercepted_prev.</td></tr><tr><td>ssli_reason_for_action</td><td>&lt;String></td><td>Read-write</td><td>SSL REASON Codes..<br>Maximum length = 255</td></tr><tr><td>user_name</td><td>&lt;String></td><td>Read-write</td><td>User Name.<br>Maximum length = 255</td></tr><tr><td>domain_name</td><td>&lt;String></td><td>Read-write</td><td>HTTP Request URL..<br>Maximum length = 2000</td></tr><tr><td>exporter_id</td><td>&lt;Double></td><td>Read-write</td><td>Exporter ID.</td></tr><tr><td>total_not_intercepted</td><td>&lt;Double></td><td>Read-write</td><td>total_not_intercepted.</td></tr><tr><td>ssli_policy_action</td><td>&lt;Double></td><td>Read-write</td><td>ssli_policy_action.</td></tr><tr><td>total_not_attempted</td><td>&lt;Double></td><td>Read-write</td><td>total_not_attempted.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/swg_ssl_details
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "swg_ssl_details":[{"ssli_executed_action":<String_value>,"__count":<Double_value>,"total_not_attempted_prev":<Double_value>,"rpt_sample_time":<Double_value>,"total_not_intercepted_prev":<Double_value>,"ssli_reason_for_action":<String_value>,"user_name":<String_value>,"domain_name":<String_value>,"exporter_id":<Double_value>,"total_not_intercepted":<Double_value>,"ssli_policy_action":<Double_value>,"total_not_attempted":<Double_value>}]}```



