#ns_ssl_csr



Configuration for CSR File resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tenant_name</td><td>&lt;String></td><td>Read-write</td><td>Tenant Name.</td></tr><tr><td>commonname</td><td>&lt;String></td><td>Read-write</td><td>Common Name.<br>Minimum length = 1</td></tr><tr><td>statename</td><td>&lt;String></td><td>Read-write</td><td>State Name.<br>Minimum length = 2<br>Maximum length = 128</td></tr><tr><td>organizationname</td><td>&lt;String></td><td>Read-write</td><td>Organization Name.<br>Minimum length = 1</td></tr><tr><td>keyform</td><td>&lt;String></td><td>Read-write</td><td>Key Form.</td></tr><tr><td>file_location_path</td><td>&lt;String></td><td>Read-write</td><td>File Location on Client for download.<br>Minimum length = 1</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>City.</td></tr><tr><td>file_name</td><td>&lt;String></td><td>Read-write</td><td>Name for and, optionally, path to the certificate signing request (CSR).<br>Minimum length = 1<br>Maximum length = 256</td></tr><tr><td>countryname</td><td>&lt;String></td><td>Read-write</td><td>Country Name.<br>Minimum length = 2<br>Maximum length = 128</td></tr><tr><td>csr</td><td>&lt;String></td><td>Read-write</td><td>Generated CSR.</td></tr><tr><td>keyfile</td><td>&lt;String></td><td>Read-write</td><td>Key File.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>passphrase</td><td>&lt;String></td><td>Read-write</td><td>Pass Phrase used to encrypt the private-key.</td></tr><tr><td>file_size</td><td>&lt;Integer></td><td>Read-only</td><td>file_size.</td></tr><tr><td>file_last_modified</td><td>&lt;String></td><td>Read-only</td><td>Last Modified.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPLOAD](#u)| [DOWNLOAD](#dow)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_csr?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{ns_ssl_csr: {
<b>"commonname":<String_value></b>,
<b>"statename":<String_value></b>,
<b>"organizationname":<String_value></b>,
<b>"file_name":<String_value></b>,
<b>"countryname":<String_value></b>,
<b>"keyfile":<String_value></b>,
"keyform":<String_value>,
"city":<String_value>,
"passphrase":<String_value>,
"tenant_name":<String_value>,
"file_location_path":<String_value>,
"csr":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_csr":[{
"tenant_name":<String_value>,
"commonname":<String_value>,
"statename":<String_value>,
"file_size":<Integer_value>,
"organizationname":<String_value>,
"file_last_modified":<String_value>,
"keyform":<String_value>,
"is_dir":<Boolean_value>,
"file_location_path":<String_value>,
"city":<String_value>,
"file_name":<String_value>,
"countryname":<String_value>,
"csr":<String_value>,
"keyfile":<String_value>,
"passphrase":<String_value>}]}
```







###delete







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_csr/file_name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_csr

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_csr":[{
"tenant_name":<String_value>,
"commonname":<String_value>,
"statename":<String_value>,
"file_size":<Integer_value>,
"organizationname":<String_value>,
"file_last_modified":<String_value>,
"keyform":<String_value>,
"is_dir":<Boolean_value>,
"file_location_path":<String_value>,
"city":<String_value>,
"file_name":<String_value>,
"countryname":<String_value>,
"csr":<String_value>,
"keyfile":<String_value>,
"passphrase":<String_value>}]}
```







###get







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_csr/file_name_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_csr":[{
"tenant_name":<String_value>,
"commonname":<String_value>,
"statename":<String_value>,
"file_size":<Integer_value>,
"organizationname":<String_value>,
"file_last_modified":<String_value>,
"keyform":<String_value>,
"is_dir":<Boolean_value>,
"file_location_path":<String_value>,
"city":<String_value>,
"file_name":<String_value>,
"countryname":<String_value>,
"csr":<String_value>,
"keyfile":<String_value>,
"passphrase":<String_value>}]}
```







###upload







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/upload/ns_ssl_csr

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done }
```







###download







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/download/ns_ssl_csr/file_name_value&lt;String&gt;

<b>HTTP Method:</b>null







