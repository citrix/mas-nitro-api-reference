#web_detail_data_collection_config



Configuration for web detail data collection config resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>name.</td></tr><tr><td>network_latency_client_side</td><td>&lt;Double></td><td>Read-write</td><td>Network Latency Client side Time should be greate than value or equal to .(millisec).</td></tr><tr><td>server_response_time</td><td>&lt;Double></td><td>Read-write</td><td>Server Response Time should be greate than or equal to value.(millisec).</td></tr><tr><td>max_first_level_number_of_record</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of record to be maintained at first level report..</td></tr><tr><td>network_latency_server_side</td><td>&lt;Double></td><td>Read-write</td><td>Network Latency Client server Time should be greate than or equal to value.(millisec).</td></tr><tr><td>application_response_time</td><td>&lt;Double></td><td>Read-write</td><td>Application Response Time should be greater than or equal to value. (millisec).</td></tr><tr><td>http_rsp_status_2xx_enabled</td><td>&lt;Integer></td><td>Read-write</td><td>HTTP Response Status Method collect enabled for 2xx response..</td></tr><tr><td>max_second_level_number_of_record</td><td>&lt;Double></td><td>Read-write</td><td>Maximum number of record to be maintained except at first level report..</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/web_detail_data_collection_config

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "web_detail_data_collection_config":[{
"name":<String_value>,
"network_latency_client_side":<Double_value>,
"server_response_time":<Double_value>,
"max_first_level_number_of_record":<Double_value>,
"network_latency_server_side":<Double_value>,
"application_response_time":<Double_value>,
"http_rsp_status_2xx_enabled":<Integer_value>,
"max_second_level_number_of_record":<Double_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/web_detail_data_collection_config/name_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "web_detail_data_collection_config":[{
"name":<String_value>,
"network_latency_client_side":<Double_value>,
"server_response_time":<Double_value>,
"max_first_level_number_of_record":<Double_value>,
"network_latency_server_side":<Double_value>,
"application_response_time":<Double_value>,
"http_rsp_status_2xx_enabled":<Integer_value>,
"max_second_level_number_of_record":<Double_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/web_detail_data_collection_config/name_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{web_detail_data_collection_config:{
<b>"name":<String_value></b>,
<b>"application_response_time":<Double_value></b>,
"http_rsp_status_2xx_enabled":<Integer_value>,
"max_second_level_number_of_record":<Double_value>,
"server_response_time":<Double_value>,
"network_latency_server_side":<Double_value>,
"network_latency_client_side":<Double_value>,
"max_first_level_number_of_record":<Double_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "web_detail_data_collection_config":[{
"name":<String_value>,
"network_latency_client_side":<Double_value>,
"server_response_time":<Double_value>,
"max_first_level_number_of_record":<Double_value>,
"network_latency_server_side":<Double_value>,
"application_response_time":<Double_value>,
"http_rsp_status_2xx_enabled":<Integer_value>,
"max_second_level_number_of_record":<Double_value>}]}
```







