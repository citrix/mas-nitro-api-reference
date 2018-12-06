#perf_ssl_backend_ciphers_report



Configuration for SSL Back-end Ciphers report resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sslbkendcipheraes256rate</td><td>&lt;Double></td><td>Read-write</td><td>sslbkendcipheraes256rate Value .</td></tr><tr><td>sslbe40bitdesciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe40bitdesciphersrate Value .</td></tr><tr><td>sslbe56bitdesciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe56bitdesciphersrate Value .</td></tr><tr><td>sslbe168bit3desciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe168bit3desciphersrate Value .</td></tr><tr><td>sslbe40bitrc2ciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe40bitrc2ciphersrate Value .</td></tr><tr><td>timestamp</td><td>&lt;Double></td><td>Read-write</td><td>timestamp in milliseconds.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the entries in this perf table configuration.<br>Maximum length = 256</td></tr><tr><td>sslbe128bitrc4ciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe128bitrc4ciphersrate Value .</td></tr><tr><td>sslbenullciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbenullciphersrate Value .</td></tr><tr><td>sslbe64bitrc4ciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe64bitrc4ciphersrate Value .</td></tr><tr><td>sslbe56bitrc2ciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe56bitrc2ciphersrate Value .</td></tr><tr><td>sslbe40bitrc4ciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe40bitrc4ciphersrate Value.</td></tr><tr><td>device_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Device IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>sslbe128bitrc2ciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe128bitrc2ciphersrate Value .</td></tr><tr><td>sslbkendcipheraes128rate</td><td>&lt;Double></td><td>Read-write</td><td>sslbkendcipheraes128rate Value .</td></tr><tr><td>sslbe56bitrc4ciphersrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbe56bitrc4ciphersrate Value .</td></tr><tr><td>report_start_time</td><td>&lt;Double></td><td>Read-write</td><td>report_start_time in seconds.</td></tr><tr><td>report_end_time</td><td>&lt;Double></td><td>Read-write</td><td>report_end_time in seconds.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[GET](#get)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_ssl_backend_ciphers_report

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_ssl_backend_ciphers_report":[{
"sslbkendcipheraes256rate":<Double_value>,
"sslbe40bitdesciphersrate":<Double_value>,
"sslbe56bitdesciphersrate":<Double_value>,
"sslbe168bit3desciphersrate":<Double_value>,
"sslbe40bitrc2ciphersrate":<Double_value>,
"timestamp":<Double_value>,
"id":<String_value>,
"sslbe128bitrc4ciphersrate":<Double_value>,
"sslbenullciphersrate":<Double_value>,
"sslbe64bitrc4ciphersrate":<Double_value>,
"sslbe56bitrc2ciphersrate":<Double_value>,
"sslbe40bitrc4ciphersrate":<Double_value>,
"device_ip_address":<String_value>,
"sslbe128bitrc2ciphersrate":<Double_value>,
"sslbkendcipheraes128rate":<Double_value>,
"sslbe56bitrc4ciphersrate":<Double_value>,
"report_start_time":<Double_value>,
"report_end_time":<Double_value>}]}
```







