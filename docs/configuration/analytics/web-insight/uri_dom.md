#uri_dom

Configuration for AF URL dom Report table for Level 1 resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>embedded_object_count</td><td>&lt;Double></td><td>Read-write</td><td>embedded_object_count.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>count..</td></tr><tr><td>max_transaction_time</td><td>&lt;Double></td><td>Read-write</td><td>Last Transaction Time for this URL in the sampled timeframe..</td></tr><tr><td>complete_rendering_time</td><td>&lt;Double></td><td>Read-write</td><td>Render time..</td></tr><tr><td>response_send_time</td><td>&lt;Double></td><td>Read-write</td><td>response_send_time.</td></tr><tr><td>start_rendering_time</td><td>&lt;Double></td><td>Read-write</td><td>Render time..</td></tr><tr><td>render_time</td><td>&lt;Double></td><td>Read-write</td><td>Render time..</td></tr><tr><td>request_time_to_first_byte</td><td>&lt;Double></td><td>Read-write</td><td>request_time_to_first_byte.</td></tr><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>HTTP Request URL..<br>Maximum length = 2000</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is URL Dom..<br>Maximum length = 2000</td></tr><tr><td>rpt_sample_time</td><td>&lt;Double></td><td>Read-write</td><td>Report Sample time..</td></tr><tr><td>x_scale</td><td>&lt;Double></td><td>Read-write</td><td>x_scale.</td></tr><tr><td>request_processing_time</td><td>&lt;Double></td><td>Read-write</td><td>request_processing_time.</td></tr><tr><td>load_time</td><td>&lt;Double></td><td>Read-write</td><td>URI Load time..</td></tr><tr><td>is_embedded_object</td><td>&lt;Double></td><td>Read-write</td><td>is_embedded_object.</td></tr><tr><td>application_response_time</td><td>&lt;Double></td><td>Read-write</td><td>Application Response Time..</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/uri_dom
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "uri_dom":[{"embedded_object_count":<Double_value>,"__count":<Double_value>,"http_resp_status_name":<String_value>,"max_transaction_time":<Double_value>,"complete_rendering_time":<Double_value>,"response_send_time":<Double_value>,"start_rendering_time":<Double_value>,"app_unit_name":<String_value>,"render_time":<Double_value>,"request_time_to_first_byte":<Double_value>,"url":<String_value>,"id":<String_value>,"operating_system_name":<String_value>,"server_ip_address":<String_value>,"http_req_method_name":<String_value>,"rpt_sample_time":<Double_value>,"user_agent_name":<String_value>,"x_scale":<Double_value>,"device_ip_address":<String_value>,"domain_name":<String_value>,"request_processing_time":<Double_value>,"load_time":<Double_value>,"is_embedded_object":<Double_value>,"client_ip_address":<String_value>,"application_response_time":<Double_value>}]}```



