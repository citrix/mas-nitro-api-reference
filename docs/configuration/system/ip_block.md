#ip_block



Configuration for This collection holds private ip block information. resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>longitude</td><td>&lt;Double></td><td>Read-write</td><td>longitude.</td></tr><tr><td>region_code</td><td>&lt;String></td><td>Read-write</td><td>region_code.<br>Maximum length = 16</td></tr><tr><td>end_ip_num</td><td>&lt;Double></td><td>Read-write</td><td>end_ip_num.</td></tr><tr><td>country_code</td><td>&lt;String></td><td>Read-write</td><td>country_code.<br>Maximum length = 256</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>name.<br>Minimum length = 1<br>Maximum length = 256</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Description about Ip Block.<br>Maximum length = 256</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>city.<br>Maximum length = 256</td></tr><tr><td>latitude</td><td>&lt;Double></td><td>Read-write</td><td>latitude.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is IP block name.<br>Maximum length = 256</td></tr><tr><td>start_ip_num</td><td>&lt;Double></td><td>Read-write</td><td>start_ip_num.</td></tr><tr><td>custom_city</td><td>&lt;Boolean></td><td>Read-write</td><td>custom_city.</td></tr><tr><td>custom_country</td><td>&lt;Boolean></td><td>Read-write</td><td>custom_country.</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>country.<br>Maximum length = 256</td></tr><tr><td>end_ip</td><td>&lt;String></td><td>Read-write</td><td>end_ip.</td></tr><tr><td>start_ip</td><td>&lt;String></td><td>Read-write</td><td>start_ip.</td></tr><tr><td>custom_region</td><td>&lt;Boolean></td><td>Read-write</td><td>custom_region.</td></tr><tr><td>region</td><td>&lt;String></td><td>Read-write</td><td>region.<br>Maximum length = 256</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-only</td><td>Tenant Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ip_block?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ip_block: {
"custom_city":<Boolean_value>,
"country_code":<String_value>,
"end_ip":<String_value>,
"latitude":<Double_value>,
"start_ip_num":<Double_value>,
"id":<String_value>,
"longitude":<Double_value>,
"custom_region":<Boolean_value>,
"end_ip_num":<Double_value>,
"region_code":<String_value>,
"region":<String_value>,
"name":<String_value>,
"description":<String_value>,
"city":<String_value>,
"country":<String_value>,
"start_ip":<String_value>,
"custom_country":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ip_block":[{
"longitude":<Double_value>,
"region_code":<String_value>,
"end_ip_num":<Double_value>,
"country_code":<String_value>,
"name":<String_value>,
"description":<String_value>,
"tenant_id":<String_value>,
"city":<String_value>,
"latitude":<Double_value>,
"id":<String_value>,
"start_ip_num":<Double_value>,
"custom_city":<Boolean_value>,
"custom_country":<Boolean_value>,
"country":<String_value>,
"end_ip":<String_value>,
"start_ip":<String_value>,
"custom_region":<Boolean_value>,
"region":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ip_block/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ip_block

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ip_block":[{
"longitude":<Double_value>,
"region_code":<String_value>,
"end_ip_num":<Double_value>,
"country_code":<String_value>,
"name":<String_value>,
"description":<String_value>,
"tenant_id":<String_value>,
"city":<String_value>,
"latitude":<Double_value>,
"id":<String_value>,
"start_ip_num":<Double_value>,
"custom_city":<Boolean_value>,
"custom_country":<Boolean_value>,
"country":<String_value>,
"end_ip":<String_value>,
"start_ip":<String_value>,
"custom_region":<Boolean_value>,
"region":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ip_block/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ip_block":[{
"longitude":<Double_value>,
"region_code":<String_value>,
"end_ip_num":<Double_value>,
"country_code":<String_value>,
"name":<String_value>,
"description":<String_value>,
"tenant_id":<String_value>,
"city":<String_value>,
"latitude":<Double_value>,
"id":<String_value>,
"start_ip_num":<Double_value>,
"custom_city":<Boolean_value>,
"custom_country":<Boolean_value>,
"country":<String_value>,
"end_ip":<String_value>,
"start_ip":<String_value>,
"custom_region":<Boolean_value>,
"region":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ip_block/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ip_block:{
<b>"id":<String_value></b>,
"custom_city":<Boolean_value>,
"country_code":<String_value>,
"end_ip":<String_value>,
"latitude":<Double_value>,
"start_ip_num":<Double_value>,
"longitude":<Double_value>,
"custom_region":<Boolean_value>,
"end_ip_num":<Double_value>,
"region_code":<String_value>,
"region":<String_value>,
"name":<String_value>,
"description":<String_value>,
"city":<String_value>,
"country":<String_value>,
"start_ip":<String_value>,
"custom_country":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ip_block":[{
"longitude":<Double_value>,
"region_code":<String_value>,
"end_ip_num":<Double_value>,
"country_code":<String_value>,
"name":<String_value>,
"description":<String_value>,
"tenant_id":<String_value>,
"city":<String_value>,
"latitude":<Double_value>,
"id":<String_value>,
"start_ip_num":<Double_value>,
"custom_city":<Boolean_value>,
"custom_country":<Boolean_value>,
"country":<String_value>,
"end_ip":<String_value>,
"start_ip":<String_value>,
"custom_region":<Boolean_value>,
"region":<String_value>}]}
```







