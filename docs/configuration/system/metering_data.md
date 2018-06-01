#metering_data

Configuration for Metering Data for VM Devices resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the metering data points.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address for this VM device for which data is recorded.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>interval_txmbits</td><td>&lt;Double></td><td>Read-only</td><td>Out Tx of VM Instance for Interval in Mbits.</td></tr><tr><td>burst_thpt</td><td>&lt;Double></td><td>Read-only</td><td>Burst Throughput of VM Instance in Mbps.</td></tr><tr><td>tx</td><td>&lt;Double></td><td>Read-only</td><td>Out Throughput of VM Instance in Mbps.</td></tr><tr><td>rx</td><td>&lt;Double></td><td>Read-only</td><td>In Throughput of VM Instance in Mbps.</td></tr><tr><td>start_time</td><td>&lt;Double></td><td>Read-only</td><td>Start Time of Interval for which data was recorded.</td></tr><tr><td>min_thpt</td><td>&lt;Double></td><td>Read-only</td><td>Minimum Throughput allocated to Instance in Mbps.</td></tr><tr><td>interval_rxmbits</td><td>&lt;Double></td><td>Read-only</td><td>In Rx of VM Instance for Interval in Mbits.</td></tr><tr><td>poll_time</td><td>&lt;Double></td><td>Read-only</td><td>Poll Time at which data was recorded.</td></tr><tr><td>max_thpt_limit</td><td>&lt;Double></td><td>Read-only</td><td>Maximum Throughput Limit allowed for VM Instance in Mbps.</td></tr><tr><td>total_txmbits</td><td>&lt;Double></td><td>Read-only</td><td>Out Total Rx of VM Instance in Mbits.</td></tr><tr><td>thpt_limit</td><td>&lt;Double></td><td>Read-only</td><td>Throughput Limit configured for VM Instance in Mbps.</td></tr><tr><td>total_rxmbits</td><td>&lt;Double></td><td>Read-only</td><td>In Total Rx of VM Instance in Mbits.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[PRUNE](#)| [GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###prune



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/metering_data/id_value&lt;String&gt;?action=prune;onerror=&lt;String_value&gt;
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{"metering_data": { }}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>}```



###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/metering_data
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "metering_data":[{"interval_txmbits":<Double_value>,"burst_thpt":<Double_value>,"tx":<Double_value>,"rx":<Double_value>,"start_time":<Double_value>,"min_thpt":<Double_value>,"interval_rxmbits":<Double_value>,"poll_time":<Double_value>,"max_thpt_limit":<Double_value>,"total_txmbits":<Double_value>,"thpt_limit":<Double_value>,"total_rxmbits":<Double_value>,"id":<String_value>,"ip_address":<String_value>}]}```



