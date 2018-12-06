#mps_ssl_certkey



Configuration for Install SSL certificate on Management Service resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>The pass-phrase that was used to encrypt the private-key..<br>Maximum length = 32</td></tr><tr><td>ssl_key</td><td>&lt;String></td><td>Read-write</td><td>Key.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>ssl_certificate</td><td>&lt;String></td><td>Read-write</td><td>Certificate.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>fingerprint</td><td>&lt;String></td><td>Read-write</td><td>SHA-1 Fingerprint of MAS SSL Certificate.<br>Minimum length = 1<br>Maximum length = 512</td></tr><tr><td>serial_number</td><td>&lt;String></td><td>Read-only</td><td>Serial Number.</td></tr><tr><td>signature_algorithm</td><td>&lt;String></td><td>Read-only</td><td>Signature Algorithm.</td></tr><tr><td>valid_from</td><td>&lt;String></td><td>Read-only</td><td>Valid From.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Tells whether the certificate is still valid or not.</td></tr><tr><td>issuer</td><td>&lt;String></td><td>Read-only</td><td>Issuer.</td></tr><tr><td>public_key_size</td><td>&lt;Integer></td><td>Read-only</td><td>Public Key Size.</td></tr><tr><td>valid_to</td><td>&lt;String></td><td>Read-only</td><td>Valid To.</td></tr><tr><td>version</td><td>&lt;String></td><td>Read-only</td><td>Version.</td></tr><tr><td>subject</td><td>&lt;String></td><td>Read-only</td><td>Subject.</td></tr><tr><td>public_key_algorithm</td><td>&lt;String></td><td>Read-only</td><td>Public Key Algorithm.</td></tr><tr><td>days_to_expiry</td><td>&lt;Integer></td><td>Read-only</td><td>Days before SSL certificate expires.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [GET (ALL)](#get-all)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_ssl_certkey?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{mps_ssl_certkey: {
<b>"ssl_certificate":<String_value></b>,
"fingerprint":<String_value>,
"password":<String_value>,
"ssl_key":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"issuer":<String_value>,
"public_key_size":<Integer_value>,
"password":<String_value>,
"ssl_key":<String_value>,
"valid_to":<String_value>,
"reboot":<Boolean_value>,
"version":<String_value>,
"subject":<String_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"ssl_certificate":<String_value>,
"cert_format":<String_value>,
"fingerprint":<String_value>}]}
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/mps_ssl_certkey

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "mps_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"issuer":<String_value>,
"public_key_size":<Integer_value>,
"password":<String_value>,
"ssl_key":<String_value>,
"valid_to":<String_value>,
"reboot":<Boolean_value>,
"version":<String_value>,
"subject":<String_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"ssl_certificate":<String_value>,
"cert_format":<String_value>,
"fingerprint":<String_value>}]}
```







