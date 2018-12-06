#ns_ssl_certkey



Configuration for SSL certificate on NetScaler resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>no_domain_check</td><td>&lt;Boolean></td><td>Read-write</td><td>Specify this option to override the check for matching domain names during certificate update operation.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>List of NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>certkeypair_name</td><td>&lt;String></td><td>Read-write</td><td>Cert Key Pair Name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>ssl_key</td><td>&lt;String></td><td>Read-write</td><td>Key.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for all ssl cert-keys entries. For download operation "id" must be provided in the format ;ltns_ip_address&gt;_;ltcertkeypair_name&gt;.tgz.</td></tr><tr><td>key_data</td><td>&lt;String></td><td>Read-write</td><td>Key Data.<br>Maximum length = 16384</td></tr><tr><td>ssl_certificate</td><td>&lt;String></td><td>Read-write</td><td>Certificate.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>certificate_data</td><td>&lt;String></td><td>Read-write</td><td>Certificate Data.<br>Maximum length = 16384</td></tr><tr><td>file_location_path</td><td>&lt;String></td><td>Read-write</td><td>File Location on Client for download.<br>Minimum length = 1</td></tr><tr><td>cert_format</td><td>&lt;String></td><td>Read-write</td><td>Certificate Format.<br>Maximum length = 64</td></tr><tr><td>certchainbinding</td><td>&lt;String[]></td><td>Read-write</td><td>Certificate Chain binding..</td></tr><tr><td>save_config</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if save config is required.</td></tr><tr><td>source_certificate</td><td>&lt;String></td><td>Read-write</td><td>CertKeyPair Name of the certificate that needs to installed in another instance.</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>The pass-phrase that was used to encrypt the private-key..<br>Maximum length = 128</td></tr><tr><td>source_ipaddress</td><td>&lt;String></td><td>Read-write</td><td>NS IP of the certificate that needs to installed in another instance.</td></tr><tr><td>ns_ip_address_arr</td><td>&lt;String[]></td><td>Read-write</td><td>List of NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>serial_number</td><td>&lt;String></td><td>Read-only</td><td>Serial Number.</td></tr><tr><td>signature_algorithm</td><td>&lt;String></td><td>Read-only</td><td>Signature Algorithm.</td></tr><tr><td>valid_from</td><td>&lt;String></td><td>Read-only</td><td>Valid From.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-only</td><td>Tells whether the certificate is still valid or not.</td></tr><tr><td>hostname</td><td>&lt;String></td><td>Read-only</td><td>Host Name of the device.</td></tr><tr><td>issuer</td><td>&lt;String></td><td>Read-only</td><td>Issuer.</td></tr><tr><td>public_key_size</td><td>&lt;Integer></td><td>Read-only</td><td>Public Key Size.</td></tr><tr><td>device_name</td><td>&lt;String></td><td>Read-only</td><td>Name of the device.</td></tr><tr><td>valid_to</td><td>&lt;String></td><td>Read-only</td><td>Valid To.</td></tr><tr><td>subject</td><td>&lt;String></td><td>Read-only</td><td>Subject.</td></tr><tr><td>version</td><td>&lt;Integer></td><td>Read-only</td><td>Version.</td></tr><tr><td>public_key_algorithm</td><td>&lt;String></td><td>Read-only</td><td>Public Key Algorithm.</td></tr><tr><td>days_to_expiry</td><td>&lt;Integer></td><td>Read-only</td><td>Days before SSL certificate expires.</td></tr><tr><td>poll_time</td><td>&lt;Integer></td><td>Read-only</td><td>Last Polling Time.</td></tr><tr><td>display_name</td><td>&lt;String></td><td>Read-only</td><td>Display Name of the device.</td></tr><tr><td>no_of_bound_entities</td><td>&lt;Integer></td><td>Read-only</td><td>no_of_bound_entities.</td></tr><tr><td>partition_name</td><td>&lt;String></td><td>Read-only</td><td>Name of Admin Partition. Blank means Default Partition.</td></tr><tr><td>csr</td><td>&lt;String></td><td>Read-only</td><td>Certificate Signing Request.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[INVENTORY](#inventory)| [ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [DOWNLOAD_CERTS (ALL)](#download_certs-)| [MODIFY](#modify)| [GEN_CSR](#ge)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###inventory







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey?action=inventory;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_ssl_certkey: {
"certchainbinding":<String_value[]>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"password":<String_value>,
"source_certificate":<String_value>,
"ssl_key":<String_value>,
"source_ipaddress":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"save_config":<Boolean_value>,
"ns_ip_address_arr":<String_value[]>,
"certificate_data":<String_value>,
"ssl_certificate":<String_value>,
"file_location_path":<String_value>,
"cert_format":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"hostname":<String_value>,
"issuer":<String_value>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"public_key_size":<Integer_value>,
"device_name":<String_value>,
"ssl_key":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"valid_to":<String_value>,
"subject":<String_value>,
"version":<Integer_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"poll_time":<Integer_value>,
"display_name":<String_value>,
"no_of_bound_entities":<Integer_value>,
"ssl_certificate":<String_value>,
"certificate_data":<String_value>,
"file_location_path":<String_value>,
"partition_name":<String_value>,
"cert_format":<String_value>,
"certchainbinding":<String_value>,
"save_config":<Boolean_value>,
"source_certificate":<String_value>,
"password":<String_value>,
"source_ipaddress":<String_value>,
"csr":<String_value>,
"ns_ip_address_arr":<String_value>}]}
```







###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_ssl_certkey: {
<b>"certkeypair_name":<String_value></b>,
<b>"ns_ip_address_arr":<String_value[]></b>,
"certchainbinding":<String_value[]>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"password":<String_value>,
"source_certificate":<String_value>,
"ssl_key":<String_value>,
"source_ipaddress":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"save_config":<Boolean_value>,
"certificate_data":<String_value>,
"ssl_certificate":<String_value>,
"file_location_path":<String_value>,
"cert_format":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"hostname":<String_value>,
"issuer":<String_value>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"public_key_size":<Integer_value>,
"device_name":<String_value>,
"ssl_key":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"valid_to":<String_value>,
"subject":<String_value>,
"version":<Integer_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"poll_time":<Integer_value>,
"display_name":<String_value>,
"no_of_bound_entities":<Integer_value>,
"ssl_certificate":<String_value>,
"certificate_data":<String_value>,
"file_location_path":<String_value>,
"partition_name":<String_value>,
"cert_format":<String_value>,
"certchainbinding":<String_value>,
"save_config":<Boolean_value>,
"source_certificate":<String_value>,
"password":<String_value>,
"source_ipaddress":<String_value>,
"csr":<String_value>,
"ns_ip_address_arr":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"hostname":<String_value>,
"issuer":<String_value>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"public_key_size":<Integer_value>,
"device_name":<String_value>,
"ssl_key":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"valid_to":<String_value>,
"subject":<String_value>,
"version":<Integer_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"poll_time":<Integer_value>,
"display_name":<String_value>,
"no_of_bound_entities":<Integer_value>,
"ssl_certificate":<String_value>,
"certificate_data":<String_value>,
"file_location_path":<String_value>,
"partition_name":<String_value>,
"cert_format":<String_value>,
"certchainbinding":<String_value>,
"save_config":<Boolean_value>,
"source_certificate":<String_value>,
"password":<String_value>,
"source_ipaddress":<String_value>,
"csr":<String_value>,
"ns_ip_address_arr":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"hostname":<String_value>,
"issuer":<String_value>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"public_key_size":<Integer_value>,
"device_name":<String_value>,
"ssl_key":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"valid_to":<String_value>,
"subject":<String_value>,
"version":<Integer_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"poll_time":<Integer_value>,
"display_name":<String_value>,
"no_of_bound_entities":<Integer_value>,
"ssl_certificate":<String_value>,
"certificate_data":<String_value>,
"file_location_path":<String_value>,
"partition_name":<String_value>,
"cert_format":<String_value>,
"certchainbinding":<String_value>,
"save_config":<Boolean_value>,
"source_certificate":<String_value>,
"password":<String_value>,
"source_ipaddress":<String_value>,
"csr":<String_value>,
"ns_ip_address_arr":<String_value>}]}
```







###download_certs (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"hostname":<String_value>,
"issuer":<String_value>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"public_key_size":<Integer_value>,
"device_name":<String_value>,
"ssl_key":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"valid_to":<String_value>,
"subject":<String_value>,
"version":<Integer_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"poll_time":<Integer_value>,
"display_name":<String_value>,
"no_of_bound_entities":<Integer_value>,
"ssl_certificate":<String_value>,
"certificate_data":<String_value>,
"file_location_path":<String_value>,
"partition_name":<String_value>,
"cert_format":<String_value>,
"certchainbinding":<String_value>,
"save_config":<Boolean_value>,
"source_certificate":<String_value>,
"password":<String_value>,
"source_ipaddress":<String_value>,
"csr":<String_value>,
"ns_ip_address_arr":<String_value>}]}
```







###modify







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_ssl_certkey:{
<b>"id":<String_value></b>,
"certchainbinding":<String_value[]>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"password":<String_value>,
"source_certificate":<String_value>,
"ssl_key":<String_value>,
"source_ipaddress":<String_value>,
"key_data":<String_value>,
"save_config":<Boolean_value>,
"ns_ip_address_arr":<String_value[]>,
"certificate_data":<String_value>,
"ssl_certificate":<String_value>,
"file_location_path":<String_value>,
"cert_format":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_ssl_certkey":[{
"serial_number":<String_value>,
"signature_algorithm":<String_value>,
"valid_from":<String_value>,
"status":<String_value>,
"hostname":<String_value>,
"issuer":<String_value>,
"no_domain_check":<Boolean_value>,
"ns_ip_address":<String_value>,
"certkeypair_name":<String_value>,
"public_key_size":<Integer_value>,
"device_name":<String_value>,
"ssl_key":<String_value>,
"id":<String_value>,
"key_data":<String_value>,
"valid_to":<String_value>,
"subject":<String_value>,
"version":<Integer_value>,
"public_key_algorithm":<String_value>,
"days_to_expiry":<Integer_value>,
"poll_time":<Integer_value>,
"display_name":<String_value>,
"no_of_bound_entities":<Integer_value>,
"ssl_certificate":<String_value>,
"certificate_data":<String_value>,
"file_location_path":<String_value>,
"partition_name":<String_value>,
"cert_format":<String_value>,
"certchainbinding":<String_value>,
"save_config":<Boolean_value>,
"source_certificate":<String_value>,
"password":<String_value>,
"source_ipaddress":<String_value>,
"csr":<String_value>,
"ns_ip_address_arr":<String_value>}]}
```







###gen_csr







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_ssl_certkey/id_value&lt;String&gt;?action=gen_csr;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{"ns_ssl_certkey": { }}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>}
```







