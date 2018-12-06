#domain



Configuration for AF Domain Report table resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>miss_count</td><td>&lt;Double></td><td>Read-write</td><td>Total time window breaches for this Domain in given sampled timeframe.</td></tr><tr><td>cache_hits</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this Domain for cache hits in given sampled timeframe..</td></tr><tr><td>http_content_type_name</td><td>&lt;String></td><td>Read-write</td><td>HTTP Content TYPE Name..<br>Maximum length = 256</td></tr><tr><td>total_bytes_cache_bypass</td><td>&lt;Double></td><td>Read-write</td><td>Cache Bypass total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>ic_non_cache_hits</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this APP for cache bypass in given sampled timeframe..</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is DomainName.<br>Maximum length = 255</td></tr><tr><td>num_of_bandwidth_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches for bandwidth to this domain in the sampled timeframe..</td></tr><tr><td>total_bytes_cache_miss</td><td>&lt;Double></td><td>Read-write</td><td>Cache Miss total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>ic_miss</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this APP for cache miss in given sampled timeframe..</td></tr><tr><td>cache_miss</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this Domain for cache miss in given sampled timeframe..</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Domain Name.<br>Maximum length = 255</td></tr><tr><td>total_bytes</td><td>&lt;Double></td><td>Read-write</td><td>Total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>percent_bw_saved</td><td>&lt;Double></td><td>Read-write</td><td>Percentage of bw save to this Domain in given sampled timeframe..</td></tr><tr><td>server_response_time</td><td>&lt;Double></td><td>Read-write</td><td>Server response time..</td></tr><tr><td>num_of_hits_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches breaches for hits to this domain in the sampled timeframe..</td></tr><tr><td>network_latency_server_side</td><td>&lt;Double></td><td>Read-write</td><td>Network latency server side..</td></tr><tr><td>application_response_time</td><td>&lt;Double></td><td>Read-write</td><td>Application response time..</td></tr><tr><td>total_bytes_ic_hits</td><td>&lt;Double></td><td>Read-write</td><td>IC Cache Hits total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>num_of_open_connections_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches for open connections to this domain in the sampled timeframe..</td></tr><tr><td>hits_breach</td><td>&lt;Double></td><td>Read-write</td><td>Hits breach values reported to this domain in the sampled timeframe..</td></tr><tr><td>total_bytes_cache_hits</td><td>&lt;Double></td><td>Read-write</td><td>Cache Hits total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>ic_no_store_reason</td><td>&lt;String></td><td>Read-write</td><td>ic_no_store_reason..<br>Maximum length = 256</td></tr><tr><td>network_latency_client_side</td><td>&lt;Double></td><td>Read-write</td><td>Network latency client side..</td></tr><tr><td>total_bytes_ic_miss</td><td>&lt;Double></td><td>Read-write</td><td>Cache Miss total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>max_transaction_time</td><td>&lt;Double></td><td>Read-write</td><td>Last Transaction Time for this URL in the sampled timeframe..</td></tr><tr><td>cache_bypass</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this Domain for cache bypass in given sampled timeframe..</td></tr><tr><td>open_connections_breach</td><td>&lt;Double></td><td>Read-write</td><td>open connection breache value reported to this domain in the sampled timeframe..</td></tr><tr><td>num_of_hits_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for hits to this domain in the sampled timeframe..</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>App Ip Address..<br>Maximum length = 255</td></tr><tr><td>netscaler_processing_time</td><td>&lt;Double></td><td>Read-write</td><td>NetScaler processing time..</td></tr><tr><td>percentage_usage</td><td>&lt;Double></td><td>Read-write</td><td>Percentage_usage of this Domain in given sampled timeframe..</td></tr><tr><td>bandwidth_breach</td><td>&lt;Double></td><td>Read-write</td><td>bandwidth breach reported values to this domain in the sampled timeframe..</td></tr><tr><td>num_of_bandwidth_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for bandwidth to this domain in the sampled timeframe..</td></tr><tr><td>ic_hits</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this APP for cache hits in given sampled timeframe..</td></tr><tr><td>num_of_open_connections_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for open connections to this domain in the sampled timeframe..</td></tr><tr><td>total_bytes_ic_reval</td><td>&lt;Double></td><td>Read-write</td><td>Cache Reval total bytes accounted by this URL in sampled timeframe..</td></tr><tr><td>response_time_breach</td><td>&lt;Double></td><td>Read-write</td><td>Response time reported breach value to this domain in the sampled timeframe..</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>miss_count_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches count exceeds the configured miss count breach threshold to this Domain.</td></tr><tr><td>ic_utilization</td><td>&lt;Double></td><td>Read-write</td><td>Total IC utilization in given sampled timeframe..</td></tr><tr><td>ic_reval</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this APP for cache bypass in given sampled timeframe..</td></tr><tr><td>num_of_response_time_breaches</td><td>&lt;Double></td><td>Read-write</td><td>No of times the timewindow breaches for response time to this domain in the sampled timeframe..</td></tr><tr><td>num_of_response_time_mcb</td><td>&lt;Double></td><td>Read-write</td><td>No of missed count breaches for response time to this domain in the sampled timeframe..</td></tr><tr><td>total_requests</td><td>&lt;Double></td><td>Read-write</td><td>Total requests to this Domain in given sampled timeframe..</td></tr><tr><td>http_media_type_name</td><td>&lt;String></td><td>Read-write</td><td>HTTP MEDIA TYPE Name..<br>Maximum length = 30</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/domain

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "domain":[{
"__count":<Double_value>,
"miss_count":<Double_value>,
"cache_hits":<Double_value>,
"http_content_type_name":<String_value>,
"total_bytes_cache_bypass":<Double_value>,
"ic_non_cache_hits":<Double_value>,
"id":<String_value>,
"num_of_bandwidth_mcb":<Double_value>,
"total_bytes_cache_miss":<Double_value>,
"operating_system_name":<String_value>,
"ic_miss":<Double_value>,
"vpn_user_name":<String_value>,
"cache_miss":<Double_value>,
"http_req_method_name":<String_value>,
"name":<String_value>,
"total_bytes":<Double_value>,
"user_agent_name":<String_value>,
"percent_bw_saved":<Double_value>,
"server_response_time":<Double_value>,
"num_of_hits_mcb":<Double_value>,
"network_latency_server_side":<Double_value>,
"client_ip_address":<String_value>,
"application_response_time":<Double_value>,
"total_bytes_ic_hits":<Double_value>,
"num_of_open_connections_mcb":<Double_value>,
"hits_breach":<Double_value>,
"total_bytes_cache_hits":<Double_value>,
"ic_no_store_reason":<String_value>,
"http_resp_status_name":<String_value>,
"network_latency_client_side":<Double_value>,
"total_bytes_ic_miss":<Double_value>,
"max_transaction_time":<Double_value>,
"uri_url":<String_value>,
"cache_bypass":<Double_value>,
"open_connections_breach":<Double_value>,
"num_of_hits_breaches":<Double_value>,
"ip_address":<String_value>,
"netscaler_processing_time":<Double_value>,
"percentage_usage":<Double_value>,
"bandwidth_breach":<Double_value>,
"num_of_bandwidth_breaches":<Double_value>,
"ic_hits":<Double_value>,
"num_of_open_connections_breaches":<Double_value>,
"total_bytes_ic_reval":<Double_value>,
"response_time_breach":<Double_value>,
"server_ip_address":<String_value>,
"rpt_sample_time":<Double_value>,
"miss_count_breaches":<Double_value>,
"device_ip_address":<String_value>,
"ic_utilization":<Double_value>,
"ic_reval":<Double_value>,
"num_of_response_time_breaches":<Double_value>,
"num_of_response_time_mcb":<Double_value>,
"total_requests":<Double_value>,
"http_media_type_name":<String_value>}]}
```







