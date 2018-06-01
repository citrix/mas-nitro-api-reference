#ica_user_session_hop_detail

Configuration for Af report for ICA User Session Hop resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>client_srtt</td><td>&lt;Double></td><td>Read-write</td><td>client Smothen RTT..</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>country_code</td><td>&lt;String></td><td>Read-write</td><td>country_code.</td></tr><tr><td>client_side_ns_delay</td><td>&lt;Double></td><td>Read-write</td><td>Clinet to Server NS delay..</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>ICA Session state..</td></tr><tr><td>client_type</td><td>&lt;String></td><td>Read-write</td><td>Client Type.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>city.</td></tr><tr><td>l7_clientside_latency</td><td>&lt;Double></td><td>Read-write</td><td>L7 clientside latency.</td></tr><tr><td>launch_duration</td><td>&lt;Double></td><td>Read-write</td><td>ica session launch duration..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is ICA Session ID.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>client_jitter</td><td>&lt;Double></td><td>Read-write</td><td>ICA User client jitter..</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>country.</td></tr><tr><td>region_code</td><td>&lt;String></td><td>Read-write</td><td>region_code.</td></tr><tr><td>clientside_packet_retransmits</td><td>&lt;Double></td><td>Read-write</td><td>Client side packet retransmits..</td></tr><tr><td>region</td><td>&lt;String></td><td>Read-write</td><td>region.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>clientside_0_win</td><td>&lt;Double></td><td>Read-write</td><td>Client side 0 window count..</td></tr><tr><td>session_setup_time</td><td>&lt;Double></td><td>Read-write</td><td>ICA Session setup time..</td></tr><tr><td>clientside_rto</td><td>&lt;Double></td><td>Read-write</td><td>clientside rto..</td></tr><tr><td>clientside_cb</td><td>&lt;Double></td><td>Read-write</td><td>clientside cb.</td></tr><tr><td>client_version</td><td>&lt;String></td><td>Read-write</td><td>Client Version.<br>Maximum length = 1024</td></tr><tr><td>session_end_time</td><td>&lt;Double></td><td>Read-write</td><td>ICA Session end time..</td></tr><tr><td>session_rtt</td><td>&lt;Double></td><td>Read-write</td><td>ICA Session rtt..</td></tr><tr><td>client_latency</td><td>&lt;Double></td><td>Read-write</td><td>ica session client latency..</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ica_user_session_hop_detail
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ica_user_session_hop_detail":[{"client_srtt":<Double_value>,"ica_user_name":<String_value>,"__count":<Double_value>,"country_code":<String_value>,"client_side_ns_delay":<Double_value>,"state":<String_value>,"client_type":<String_value>,"city":<String_value>,"l7_clientside_latency":<Double_value>,"launch_duration":<Double_value>,"id":<String_value>,"client_jitter":<Double_value>,"country":<String_value>,"region_code":<String_value>,"clientside_packet_retransmits":<Double_value>,"region":<String_value>,"rpt_sample_time":<Double_value>,"clientside_0_win":<Double_value>,"session_setup_time":<Double_value>,"clientside_rto":<Double_value>,"client_ip_address":<String_value>,"clientside_cb":<Double_value>,"client_version":<String_value>,"session_end_time":<Double_value>,"session_rtt":<Double_value>,"client_latency":<Double_value>}]}```



