#metering_summary



Configuration for Metering Data Summary resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>number_of_bursts</td><td>&lt;Integer></td><td>Read-write</td><td>Number of bursts by VM Instance in Interval.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address for this VM device for which metering data summary is required.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>max_burst</td><td>&lt;Double></td><td>Read-only</td><td>Maximum Burst Throughput of VM Instance for Interval in Mbps.</td></tr><tr><td>min_rx</td><td>&lt;Double></td><td>Read-only</td><td>Minimum In Throughput of VM Instance for Interval in Mbps.</td></tr><tr><td>start_time</td><td>&lt;Double></td><td>Read-only</td><td>Start Time of interval for which summary is generated.</td></tr><tr><td>duration</td><td>&lt;String></td><td>Read-only</td><td>Interval Duration for which summary is generated.</td></tr><tr><td>total_txmbits</td><td>&lt;Double></td><td>Read-only</td><td>Out Total Rx of VM Instance for Interval in Mbits.</td></tr><tr><td>total_rxmbits</td><td>&lt;Double></td><td>Read-only</td><td>In Total Rx of VM Instance for Interval in Mbits.</td></tr><tr><td>end_time</td><td>&lt;Double></td><td>Read-only</td><td>End Time of interval for which summary is generated.</td></tr><tr><td>max_rx</td><td>&lt;Double></td><td>Read-only</td><td>Maximum In Throughput of VM Instance for Interval in Mbps.</td></tr><tr><td>max_tx</td><td>&lt;Double></td><td>Read-only</td><td>Maximum Out Throughput of VM Instance for Interval in Mbps.</td></tr><tr><td>min_tx</td><td>&lt;Double></td><td>Read-only</td><td>Minimum Out Throughput of VM Instance for Interval in Mbps.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/metering_summary

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "metering_summary":[{
"max_burst":<Double_value>,
"min_rx":<Double_value>,
"start_time":<Double_value>,
"duration":<String_value>,
"number_of_bursts":<Integer_value>,
"total_txmbits":<Double_value>,
"total_rxmbits":<Double_value>,
"end_time":<Double_value>,
"max_rx":<Double_value>,
"max_tx":<Double_value>,
"min_tx":<Double_value>,
"ip_address":<String_value>}]}
```







