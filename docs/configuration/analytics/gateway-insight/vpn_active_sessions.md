#vpn_active_sessions

Configuration for Af report for VPN Session resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>up_time</td><td>&lt;Double></td><td>Read-write</td><td>Session Up Time.</td></tr><tr><td>session_type</td><td>&lt;String></td><td>Read-write</td><td>Session type.<br>Maximum length = 128</td></tr><tr><td>vpn_user_name</td><td>&lt;String></td><td>Read-write</td><td>Name of VPN Uer.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>total_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Total Bytes.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State (Active/Idle/Terminated).<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>bandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Avg Bandwidth..</td></tr><tr><td>session_setup_time</td><td>&lt;Double></td><td>Read-write</td><td>vpn session start time.</td></tr><tr><td>client_ip</td><td>&lt;String></td><td>Read-write</td><td>Client IP Address..<br>Maximum length = 64</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is VPN Session ID.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>os_type</td><td>&lt;String></td><td>Read-write</td><td>OS type.<br>Maximum length = 128</td></tr><tr><td>session_end_time</td><td>&lt;Double></td><td>Read-write</td><td>vpn session end time.</td></tr><tr><td>server_ip</td><td>&lt;String></td><td>Read-write</td><td>Server IP Address..<br>Maximum length = 64</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/vpn_active_sessions
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "vpn_active_sessions":[{"up_time":<Double_value>,"session_type":<String_value>,"vpn_user_name":<String_value>,"__count":<Double_value>,"total_bytes":<Double_value>,"rpt_sample_time":<Double_value>,"state":<String_value>,"device_ip_address":<String_value>,"bandwidth":<Double_value>,"session_setup_time":<Double_value>,"client_ip":<String_value>,"id":<String_value>,"os_type":<String_value>,"session_end_time":<Double_value>,"server_ip":<String_value>}]}```



