#ns_ns_mode



Configuration for NS Mode resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>rise_rhi</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if rise_rhi feature is enabled.</td></tr><tr><td>sradv</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if sradv feature is enabled.</td></tr><tr><td>pmtud</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if pmtud feature is enabled.</td></tr><tr><td>ns_ip_address</td><td>&lt;String></td><td>Read-write</td><td>NetScaler IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>dradv</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if dradv feature is enabled.</td></tr><tr><td>tcpb</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if tcpb feature is enabled.</td></tr><tr><td>fr</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if fr feature is enabled.</td></tr><tr><td>dradv6</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if dradv6 feature is enabled.</td></tr><tr><td>edge</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if edge feature is enabled.</td></tr><tr><td>usnip</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if usnip feature is enabled.</td></tr><tr><td>bridgebpdus</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if bridgebpdus feature is enabled.</td></tr><tr><td>cka</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if cka feature is enabled.</td></tr><tr><td>ulfd</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if ulfd feature is enabled.</td></tr><tr><td>rise_apbr</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if rise_apbr feature is enabled.</td></tr><tr><td>sradv6</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if sradv6 feature is enabled.</td></tr><tr><td>ns_ip_address_arr</td><td>&lt;String[]></td><td>Read-write</td><td>List of NS IP Addresses.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>mbf</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if mbf feature is enabled.</td></tr><tr><td>l3</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if l3 feature is enabled.</td></tr><tr><td>l2</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if l2 feature is enabled.</td></tr><tr><td>mediaclassification</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if mediaclassification feature is enabled.</td></tr><tr><td>iradv</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if iradv feature is enabled.</td></tr><tr><td>usip</td><td>&lt;Boolean></td><td>Read-write</td><td>true, if usip feature is enabled.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



