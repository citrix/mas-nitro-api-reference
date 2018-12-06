#tcp_interface



Configuration for AF TCP Interface Report table resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>data_volume</td><td>&lt;Double></td><td>Read-write</td><td>Data Volume in given sampled timeframe..</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>trans_count_up</td><td>&lt;Double></td><td>Read-write</td><td>Upload Transaction Count.</td></tr><tr><td>avg_upload_speed_retx</td><td>&lt;Double></td><td>Read-write</td><td>TCP Average Upload Speed (with ReTx).</td></tr><tr><td>peak_burst_rate_down</td><td>&lt;Double></td><td>Read-write</td><td>Peak Burst Download Rate.</td></tr><tr><td>avg_download_speed</td><td>&lt;Double></td><td>Read-write</td><td>TCP Average Download Speed.</td></tr><tr><td>peak_burst_rate_up_no_retx</td><td>&lt;Double></td><td>Read-write</td><td>Peak Burst Upload Rate without Retransmissions.</td></tr><tr><td>peak_burst_rate_up</td><td>&lt;Double></td><td>Read-write</td><td>Peak Burst Upload Rate.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is TCP Interface..</td></tr><tr><td>peak_burst_rate_down_no_retx</td><td>&lt;Double></td><td>Read-write</td><td>Peak Burst Download Rate without Retransmissions.</td></tr><tr><td>avg_upload_speed</td><td>&lt;Double></td><td>Read-write</td><td>TCP Average Upload Speed.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>vlan</td><td>&lt;String></td><td>Read-write</td><td>VLAN Id.</td></tr><tr><td>trans_count_down</td><td>&lt;Double></td><td>Read-write</td><td>Download Transaction Count.</td></tr><tr><td>avg_download_speed_retx</td><td>&lt;Double></td><td>Read-write</td><td>TCP Average Download Speed (with ReTx).</td></tr><tr><td>throughput</td><td>&lt;Double></td><td>Read-write</td><td>Throughput.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/tcp_interface

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "tcp_interface":[{
"data_volume":<Double_value>,
"__count":<Double_value>,
"trans_count_up":<Double_value>,
"tcp_appname":<String_value>,
"bitrate_range_end":<Double_value>,
"avg_upload_speed_retx":<Double_value>,
"direction":<String_value>,
"peak_burst_rate_down":<Double_value>,
"avg_download_speed":<Double_value>,
"peak_burst_rate_up_no_retx":<Double_value>,
"peak_burst_rate_up":<Double_value>,
"id":<String_value>,
"peak_burst_rate_down_no_retx":<Double_value>,
"avg_upload_speed":<Double_value>,
"rpt_sample_time":<Double_value>,
"vlan":<String_value>,
"port":<String_value>,
"trans_count_down":<Double_value>,
"avg_download_speed_retx":<Double_value>,
"side":<String_value>,
"opt_type":<String_value>,
"throughput":<Double_value>}]}
```







