#app_info



Configuration for app_info Resource resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>report_end_time</td><td>&lt;Double></td><td>Read-write</td><td>report_end_time for getting the logs in milliseconds.</td></tr><tr><td>anomaly_data</td><td>&lt;anomaly_item[]></td><td>Read-write</td><td>List of anomalous values and their timestamp.</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>.</td></tr><tr><td>duration</td><td>&lt;String></td><td>Read-write</td><td>Calculation frequency period daily,weekly etc.</td></tr><tr><td>anomaly_count</td><td>&lt;Integer></td><td>Read-write</td><td>Number of anomalies.</td></tr><tr><td>report_start_time</td><td>&lt;Double></td><td>Read-write</td><td>report_start_time for getting the logs in milliseconds.</td></tr><tr><td>app_unit_name</td><td>&lt;String></td><td>Read-write</td><td>Name of the Application.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>server_ip</td><td>&lt;String></td><td>Read-write</td><td>Device IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/app_info

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "app_info":[{
"report_end_time":<Double_value>,
"anomaly_data":[{
"timestamp":<Double_value>,
"parent_name":<String_value>,
"value":<Double_value>,
"counter":<String_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"rpt_sample_time":<Double_value>,
"duration":<String_value>,
"anomaly_count":<Integer_value>,
"report_start_time":<Double_value>,
"app_unit_name":<String_value>,
"id":<String_value>,
"server_ip":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/app_info/server_ip_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "app_info":[{
"report_end_time":<Double_value>,
"anomaly_data":[{
"timestamp":<Double_value>,
"parent_name":<String_value>,
"value":<Double_value>,
"counter":<String_value>,
"id":<String_value>,
"parent_id":<String_value>}],
"rpt_sample_time":<Double_value>,
"duration":<String_value>,
"anomaly_count":<Integer_value>,
"report_start_time":<Double_value>,
"app_unit_name":<String_value>,
"id":<String_value>,
"server_ip":<String_value>}]}
```







