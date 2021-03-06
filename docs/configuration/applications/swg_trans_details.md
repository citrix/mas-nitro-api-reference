#swg_trans_details



Configuration for SWG Transaction Report resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>protocol used.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>operating_system</td><td>&lt;String></td><td>Read-write</td><td>Client Operating System Name..<br>Maximum length = 255</td></tr><tr><td>http_req_method</td><td>&lt;String></td><td>Read-write</td><td>HTTP Request Method..<br>Maximum length = 255</td></tr><tr><td>total_ssl_intercepts</td><td>&lt;Double></td><td>Read-write</td><td>Total Intercepts.</td></tr><tr><td>http_rsp_status</td><td>&lt;String></td><td>Read-write</td><td>HTTP Response Status Method..<br>Maximum length = 255</td></tr><tr><td>total_bytes_in</td><td>&lt;Double></td><td>Read-write</td><td>Total bytes in.</td></tr><tr><td>url_group_category</td><td>&lt;String></td><td>Read-write</td><td>URL Group Category.</td></tr><tr><td>user_agent</td><td>&lt;String></td><td>Read-write</td><td>User Agent Name..<br>Maximum length = 255</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>port</td><td>&lt;Double></td><td>Read-write</td><td>protocol used.</td></tr><tr><td>user_name</td><td>&lt;String></td><td>Read-write</td><td>User Name.<br>Maximum length = 255</td></tr><tr><td>domain_name</td><td>&lt;String></td><td>Read-write</td><td>HTTP Request URL..<br>Maximum length = 2000</td></tr><tr><td>exporter_id</td><td>&lt;String></td><td>Read-write</td><td>Exporter ID.<br>Maximum length = 255</td></tr><tr><td>total_bytes_out</td><td>&lt;Double></td><td>Read-write</td><td>Total bytes out.</td></tr><tr><td>url_reputation</td><td>&lt;Double></td><td>Read-write</td><td>URL reputation.</td></tr><tr><td>vserver_name</td><td>&lt;String></td><td>Read-write</td><td>AppName.<br>Maximum length = 255</td></tr><tr><td>url_category</td><td>&lt;Double></td><td>Read-write</td><td>URL Category.</td></tr><tr><td>client_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Client ip address.<br>Maximum length = 255</td></tr><tr><td>total_requests</td><td>&lt;Double></td><td>Read-write</td><td>Total transactions.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/swg_trans_details

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "swg_trans_details":[{
"protocol":<String_value>,
"__count":<Double_value>,
"operating_system":<String_value>,
"http_req_method":<String_value>,
"total_ssl_intercepts":<Double_value>,
"http_rsp_status":<String_value>,
"total_bytes_in":<Double_value>,
"url_group_category":<String_value>,
"user_agent":<String_value>,
"rpt_sample_time":<Double_value>,
"port":<Double_value>,
"user_name":<String_value>,
"domain_name":<String_value>,
"exporter_id":<String_value>,
"total_bytes_out":<Double_value>,
"url_reputation":<Double_value>,
"vserver_name":<String_value>,
"url_category":<Double_value>,
"client_ip_address":<String_value>,
"total_requests":<Double_value>}]}
```







