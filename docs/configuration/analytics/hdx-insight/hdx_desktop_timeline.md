#hdx_desktop_timeline



Configuration for Af report for HDX Desktop timeline resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>client_srtt</td><td>&lt;Double></td><td>Read-write</td><td>client Smothen RTT..</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>active_session_count</td><td>&lt;Double></td><td>Read-write</td><td>active_session_count..</td></tr><tr><td>desktop_count</td><td>&lt;Double></td><td>Read-write</td><td>desktop_count..</td></tr><tr><td>ica_device_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Ica device IP Address..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>active_desktop_count</td><td>&lt;Double></td><td>Read-write</td><td>ica active_desktop_count..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is HDX Desktop username.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address..<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>duration_summary_bandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Avg Bandwidth for duration summary..</td></tr><tr><td>server_latency</td><td>&lt;Double></td><td>Read-write</td><td>server latency..</td></tr><tr><td>session_duration</td><td>&lt;Double></td><td>Read-write</td><td>session duration..</td></tr><tr><td>total_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Total bytes..</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>client_subnet</td><td>&lt;String></td><td>Read-write</td><td>Client Subnet..<br>Maximum length = 64</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>username.</td></tr><tr><td>ica_rtt</td><td>&lt;Double></td><td>Read-write</td><td>ICA rtt..</td></tr><tr><td>bandwidth</td><td>&lt;Double></td><td>Read-write</td><td>Avg Bandwidth..</td></tr><tr><td>server_srtt</td><td>&lt;Double></td><td>Read-write</td><td>server Smothen RTT..</td></tr><tr><td>selected_time_total_byte</td><td>&lt;Double></td><td>Read-write</td><td>Total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>client_latency</td><td>&lt;Double></td><td>Read-write</td><td>client latency..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/hdx_desktop_timeline

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "hdx_desktop_timeline":[{
"client_srtt":<Double_value>,
"__count":<Double_value>,
"active_session_count":<Double_value>,
"desktop_count":<Double_value>,
"ica_device_ip_address":<String_value>,
"active_desktop_count":<Double_value>,
"id":<String_value>,
"ip_address":<String_value>,
"duration_summary_bandwidth":<Double_value>,
"server_latency":<Double_value>,
"session_duration":<Double_value>,
"total_bytes":<Double_value>,
"rpt_sample_time":<Double_value>,
"client_subnet":<String_value>,
"username":<String_value>,
"ica_rtt":<Double_value>,
"bandwidth":<Double_value>,
"server_srtt":<Double_value>,
"selected_time_total_byte":<Double_value>,
"client_latency":<Double_value>}]}
```







