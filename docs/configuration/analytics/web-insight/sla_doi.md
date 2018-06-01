#sla_doi

Configuration for AF SLA Domain of Interest Breaches Report table resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>hits_breach</td><td>&lt;Double></td><td>Read-write</td><td>Hits breach values reported to this domain in the sampled timeframe..</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>miss_count</td><td>&lt;Double></td><td>Read-write</td><td>Total time window breaches for this Domain in given sampled timeframe.</td></tr><tr><td>conf_miss_count</td><td>&lt;Double></td><td>Read-write</td><td>configured miss count breach to this domain.</td></tr><tr><td>open_connections_breach</td><td>&lt;Double></td><td>Read-write</td><td>open connection breache value reported to this domain in the sampled timeframe..</td></tr><tr><td>num_of_hits_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for hits to this domain in the sampled timeframe..</td></tr><tr><td>sla_sub_domain_name</td><td>&lt;String></td><td>Read-write</td><td>Sub Domain Name..<br>Maximum length = 1500</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is DomainName.<br>Maximum length = 255</td></tr><tr><td>num_of_bandwidth_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches for bandwidth to this domain in the sampled timeframe..</td></tr><tr><td>bandwidth_breach</td><td>&lt;Double></td><td>Read-write</td><td>bandwidth breach reported values to this domain in the sampled timeframe..</td></tr><tr><td>num_of_bandwidth_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for bandwidth to this domain in the sampled timeframe..</td></tr><tr><td>num_of_open_connections_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for open connections to this domain in the sampled timeframe..</td></tr><tr><td>response_time_breach</td><td>&lt;Double></td><td>Read-write</td><td>Response time reported breach value to this domain in the sampled timeframe..</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Domain Name.<br>Maximum length = 255</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>conf_time_window</td><td>&lt;Double></td><td>Read-write</td><td>configured time window breach to this domain.</td></tr><tr><td>miss_count_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches count exceeds the configured miss count breach threshold to this Domain.</td></tr><tr><td>conf_range</td><td>&lt;String></td><td>Read-write</td><td>SLA Meetric Range..<br>Maximum length = 255</td></tr><tr><td>num_of_hits_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches breaches for hits to this domain in the sampled timeframe..</td></tr><tr><td>num_of_response_time_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for response time to this domain in the sampled timeframe..</td></tr><tr><td>num_of_response_time_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches for response time to this domain in the sampled timeframe..</td></tr><tr><td>num_of_open_connections_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches for open connections to this domain in the sampled timeframe..</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/sla_doi
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "sla_doi":[{"hits_breach":<Double_value>,"__count":<Double_value>,"miss_count":<Double_value>,"conf_miss_count":<Double_value>,"open_connections_breach":<Double_value>,"num_of_hits_breaches":<Double_value>,"sla_sub_domain_name":<String_value>,"id":<String_value>,"num_of_bandwidth_mcb":<Double_value>,"bandwidth_breach":<Double_value>,"num_of_bandwidth_breaches":<Double_value>,"num_of_open_connections_breaches":<Double_value>,"response_time_breach":<Double_value>,"name":<String_value>,"rpt_sample_time":<Double_value>,"conf_time_window":<Double_value>,"miss_count_breaches":<Double_value>,"exporter_id":<String_value>,"conf_range":<String_value>,"num_of_hits_mcb":<Double_value>,"num_of_response_time_breaches":<Double_value>,"num_of_response_time_mcb":<Double_value>,"num_of_open_connections_mcb":<Double_value>}]}```



