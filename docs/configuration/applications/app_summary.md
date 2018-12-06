#app_summary



Configuration for APP Report table resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>app_threat_index</td><td>&lt;Double></td><td>Read-write</td><td>Threat Index.</td></tr><tr><td>request_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Session request bytes.</td></tr><tr><td>health_score_prev</td><td>&lt;Double></td><td>Read-write</td><td>App Health Score.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>srvr_connections_prev</td><td>&lt;Double></td><td>Read-write</td><td>Current Server Connections.</td></tr><tr><td>app_safety_index_prev</td><td>&lt;Double></td><td>Read-write</td><td>Safety Index.</td></tr><tr><td>pkt_recvd</td><td>&lt;Double></td><td>Read-write</td><td>Total Pkts Received.</td></tr><tr><td>appname</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>response_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Session response bytes.</td></tr><tr><td>total_attacks_prev</td><td>&lt;Double></td><td>Read-write</td><td>Total Attacks.</td></tr><tr><td>vslbhealth</td><td>&lt;Integer></td><td>Read-write</td><td>Vserver Health.</td></tr><tr><td>appcategory</td><td>&lt;String></td><td>Read-write</td><td>App Category.<br>Maximum length = 255</td></tr><tr><td>app_safety_index</td><td>&lt;Double></td><td>Read-write</td><td>Safety Index.</td></tr><tr><td>clnt_connections</td><td>&lt;Double></td><td>Read-write</td><td>Current Client Connections.</td></tr><tr><td>throughput_prev</td><td>&lt;Double></td><td>Read-write</td><td>Throughput ..</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>total_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Session total bytes.</td></tr><tr><td>srvr_connections</td><td>&lt;Double></td><td>Read-write</td><td>Current Server Connections.</td></tr><tr><td>total_attacks</td><td>&lt;Double></td><td>Read-write</td><td>Total Attacks.</td></tr><tr><td>total_bytes_prev</td><td>&lt;Double></td><td>Read-write</td><td>Session total bytes.</td></tr><tr><td>vservername</td><td>&lt;String></td><td>Read-write</td><td>Vserver Name.<br>Maximum length = 255</td></tr><tr><td>exporter_id</td><td>&lt;String></td><td>Read-write</td><td>Exporter ID.<br>Maximum length = 255</td></tr><tr><td>clnt_connections_prev</td><td>&lt;Double></td><td>Read-write</td><td>Current Client Connections.</td></tr><tr><td>total_requests_prev</td><td>&lt;Double></td><td>Read-write</td><td>Total Requests.</td></tr><tr><td>app_threat_index_prev</td><td>&lt;Double></td><td>Read-write</td><td>Threat Index.</td></tr><tr><td>throughput</td><td>&lt;Double></td><td>Read-write</td><td>Throughput ..</td></tr><tr><td>health_score</td><td>&lt;Double></td><td>Read-write</td><td>App Health Score.</td></tr><tr><td>total_requests</td><td>&lt;Double></td><td>Read-write</td><td>Total Requests.</td></tr><tr><td>pkt_sent</td><td>&lt;Double></td><td>Read-write</td><td>Total Pkts Sent.</td></tr><tr><td>app_family</td><td>&lt;String></td><td>Read-write</td><td>Application Family.</td></tr><tr><td>application_class</td><td>&lt;String></td><td>Read-only</td><td>Application class.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/app_summary

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "app_summary":[{
"app_threat_index":<Double_value>,
"request_bytes":<Double_value>,
"health_score_prev":<Double_value>,
"__count":<Double_value>,
"srvr_connections_prev":<Double_value>,
"app_safety_index_prev":<Double_value>,
"pkt_recvd":<Double_value>,
"appname":<String_value>,
"response_bytes":<Double_value>,
"total_attacks_prev":<Double_value>,
"vslbhealth":<Integer_value>,
"appcategory":<String_value>,
"app_safety_index":<Double_value>,
"clnt_connections":<Double_value>,
"throughput_prev":<Double_value>,
"rpt_sample_time":<Double_value>,
"total_bytes":<Double_value>,
"srvr_connections":<Double_value>,
"total_attacks":<Double_value>,
"total_bytes_prev":<Double_value>,
"vservername":<String_value>,
"application_class":<String_value>,
"exporter_id":<String_value>,
"clnt_connections_prev":<Double_value>,
"total_requests_prev":<Double_value>,
"app_threat_index_prev":<Double_value>,
"throughput":<Double_value>,
"health_score":<Double_value>,
"total_requests":<Double_value>,
"pkt_sent":<Double_value>,
"app_family":<String_value>}]}
```







