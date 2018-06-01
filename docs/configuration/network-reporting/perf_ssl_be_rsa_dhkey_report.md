#perf_ssl_be_rsa_dhkey_report

Configuration for SSL Back-end RSA vs. DH Key exchanges report resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>sslbersa512keyexchangesrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbersa512keyexchangesrate Value.</td></tr><tr><td>sslbedh2048keyexchangesrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbedh2048keyexchangesrate Value .</td></tr><tr><td>sslbersa1024keyexchangesrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbersa1024keyexchangesrate Value .</td></tr><tr><td>device_ip_address</td><td>&lt;String></td><td>Read-write</td><td>Device IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>sslbersa2048keyexchangesrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbersa2048keyexchangesrate Value .</td></tr><tr><td>timestamp</td><td>&lt;Double></td><td>Read-write</td><td>timestamp in milliseconds.</td></tr><tr><td>sslbedh1024keyexchangesrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbedh1024keyexchangesrate Value .</td></tr><tr><td>sslbedh512keyexchangesrate</td><td>&lt;Double></td><td>Read-write</td><td>sslbedh512keyexchangesrate Value .</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all the entries in this perf table configuration.<br>Maximum length = 256</td></tr><tr><td>report_start_time</td><td>&lt;Double></td><td>Read-write</td><td>report_start_time in seconds.</td></tr><tr><td>report_end_time</td><td>&lt;Double></td><td>Read-write</td><td>report_end_time in seconds.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/perf_ssl_be_rsa_dhkey_report
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "perf_ssl_be_rsa_dhkey_report":[{"sslbersa512keyexchangesrate":<Double_value>,"sslbedh2048keyexchangesrate":<Double_value>,"sslbersa1024keyexchangesrate":<Double_value>,"device_ip_address":<String_value>,"sslbersa2048keyexchangesrate":<Double_value>,"timestamp":<Double_value>,"sslbedh1024keyexchangesrate":<Double_value>,"sslbedh512keyexchangesrate":<Double_value>,"id":<String_value>,"report_start_time":<Double_value>,"report_end_time":<Double_value>}]}```



