#http_header

Configuration for Enable/Disable HTTP header info for user_agent, http_req_method, http_resp_status, operating_system as 1st level tree nodes. resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>http_content_type</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disable Http Content Type report.</td></tr><tr><td>__count</td><td>&lt;Double></td><td>Read-write</td><td>Count..</td></tr><tr><td>http_resp_status</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disable Http Resp Status report.</td></tr><tr><td>user_agent</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disable user agent report.</td></tr><tr><td>operating_system</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disbale Operating System report .</td></tr><tr><td>http_media_type</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disable Http Media Type report.</td></tr><tr><td>http_req_method</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disable http req method report.</td></tr><tr><td>domain</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disbale Domain report .</td></tr><tr><td>ic_nostore_reason</td><td>&lt;Boolean></td><td>Read-write</td><td>Enable/Disable Cache No Store Reason report.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [MODIFY](#m)


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/http_header
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "http_header":[{"http_content_type":<Boolean_value>,"__count":<Double_value>,"http_resp_status":<Boolean_value>,"user_agent":<Boolean_value>,"operating_system":<Boolean_value>,"http_media_type":<Boolean_value>,"http_req_method":<Boolean_value>,"domain":<Boolean_value>,"ic_nostore_reason":<Boolean_value>}]}```



###modify



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/http_header/
<b>HTTP Method:</b>null
<b>Request Payload: </b>```{http_header:{"domain":<Boolean_value>,"__count":<Double_value>,"http_content_type":<Boolean_value>,"user_agent":<Boolean_value>,"http_resp_status":<Boolean_value>,"ic_nostore_reason":<Boolean_value>,"operating_system":<Boolean_value>,"http_req_method":<Boolean_value>,"http_media_type":<Boolean_value>}}```
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "http_header":[{"http_content_type":<Boolean_value>,"__count":<Double_value>,"http_resp_status":<Boolean_value>,"user_agent":<Boolean_value>,"operating_system":<Boolean_value>,"http_media_type":<Boolean_value>,"http_req_method":<Boolean_value>,"domain":<Boolean_value>,"ic_nostore_reason":<Boolean_value>}]}```



