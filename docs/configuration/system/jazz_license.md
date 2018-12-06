#jazz_license



Configuration for Jazz License Information resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>date_purchased</td><td>&lt;String></td><td>Read-write</td><td>Purchase Date for license.</td></tr><tr><td>session_id</td><td>&lt;String></td><td>Read-write</td><td>Session id for license.</td></tr><tr><td>features</td><td>&lt;String></td><td>Read-write</td><td>Features for license.</td></tr><tr><td>relevance</td><td>&lt;Integer></td><td>Read-write</td><td>Relevance of license.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of license.</td></tr><tr><td>serial_no</td><td>&lt;String></td><td>Read-write</td><td>Serial Number for license.</td></tr><tr><td>count_total</td><td>&lt;Integer></td><td>Read-write</td><td>Count Total of license.</td></tr><tr><td>count_available</td><td>&lt;Integer></td><td>Read-write</td><td>Count Available of license.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>ID for license.</td></tr><tr><td>date_exp</td><td>&lt;String></td><td>Read-write</td><td>Expiry Date for license.</td></tr><tr><td>bind_type</td><td>&lt;String></td><td>Read-write</td><td>Bind Type for license.</td></tr><tr><td>use_proxy</td><td>&lt;Boolean></td><td>Read-write</td><td>Use license proxy configured to connect to citrix backoffice.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[FETCH](#)| [GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###fetch







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/jazz_license?action=fetch;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{jazz_license: {
"id":<String_value>,
"bind_type":<String_value>,
"use_proxy":<Boolean_value>,
"name":<String_value>,
"count_total":<Integer_value>,
"date_exp":<String_value>,
"session_id":<String_value>,
"date_purchased":<String_value>,
"serial_no":<String_value>,
"count_available":<Integer_value>,
"features":<String_value>,
"relevance":<Integer_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "jazz_license":[{
"date_purchased":<String_value>,
"session_id":<String_value>,
"features":<String_value>,
"relevance":<Integer_value>,
"name":<String_value>,
"serial_no":<String_value>,
"count_total":<Integer_value>,
"count_available":<Integer_value>,
"id":<String_value>,
"date_exp":<String_value>,
"bind_type":<String_value>,
"use_proxy":<Boolean_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/jazz_license

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "jazz_license":[{
"date_purchased":<String_value>,
"session_id":<String_value>,
"features":<String_value>,
"relevance":<Integer_value>,
"name":<String_value>,
"serial_no":<String_value>,
"count_total":<Integer_value>,
"count_available":<Integer_value>,
"id":<String_value>,
"date_exp":<String_value>,
"bind_type":<String_value>,
"use_proxy":<Boolean_value>}]}
```







