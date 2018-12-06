#ns_vmacs



Configuration for vmacs for shared vlans resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>vmacs</td><td>&lt;String></td><td>Read-write</td><td>Comma Seperated VMac list.<br>Minimum length = 1</td></tr><tr><td>additional_mac_free_count</td><td>&lt;Integer></td><td>Read-write</td><td>Place holder for to view additional mac count.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>increment_by</td><td>&lt;Integer></td><td>Read-write</td><td>increment by.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>generation_method</td><td>&lt;String></td><td>Read-write</td><td>(MANUAL, BASE or RANDOM).<br>Minimum length = 4<br>Maximum length = 16</td></tr><tr><td>vmac_count</td><td>&lt;Integer></td><td>Read-write</td><td>increment by.<br>Minimum value = 1</td></tr><tr><td>sync_operation</td><td>&lt;Boolean></td><td>Read-write</td><td>sync operation.</td></tr><tr><td>base_vmac</td><td>&lt;String></td><td>Read-write</td><td>Base VMac Address.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [REMOVE](#r)| [GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_vmacs?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_vmacs: {
<b>"ns_ip_address":<String_value></b>,
<b>"generation_method":<String_value></b>,
"increment_by":<Integer_value>,
"vmac_count":<Integer_value>,
"additional_mac_free_count":<Integer_value>,
"vmacs":<String_value>,
"base_vmac":<String_value>,
"sync_operation":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_vmacs":[{
"vmacs":<String_value>,
"additional_mac_free_count":<Integer_value>,
"ns_ip_address":<String_value>,
"increment_by":<Integer_value>,
"generation_method":<String_value>,
"vmac_count":<Integer_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>,
"base_vmac":<String_value>}]}
```







###remove







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_vmacs?action=remove;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_vmacs: {
"increment_by":<Integer_value>,
"vmac_count":<Integer_value>,
"additional_mac_free_count":<Integer_value>,
"ns_ip_address":<String_value>,
"generation_method":<String_value>,
"vmacs":<String_value>,
"base_vmac":<String_value>,
"sync_operation":<Boolean_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_vmacs":[{
"vmacs":<String_value>,
"additional_mac_free_count":<Integer_value>,
"ns_ip_address":<String_value>,
"increment_by":<Integer_value>,
"generation_method":<String_value>,
"vmac_count":<Integer_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>,
"base_vmac":<String_value>}]}
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_vmacs

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_vmacs":[{
"vmacs":<String_value>,
"additional_mac_free_count":<Integer_value>,
"ns_ip_address":<String_value>,
"increment_by":<Integer_value>,
"generation_method":<String_value>,
"vmac_count":<Integer_value>,
"act_id":<String_value>,
"sync_operation":<Boolean_value>,
"base_vmac":<String_value>}]}
```







