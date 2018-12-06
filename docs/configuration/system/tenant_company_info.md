#tenant_company_info



Configuration for Company Information of Tenant resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>department</td><td>&lt;String></td><td>Read-write</td><td>Department of the tenant.</td></tr><tr><td>company_name</td><td>&lt;String></td><td>Read-write</td><td>Name of the tenant company.</td></tr><tr><td>zip_code</td><td>&lt;String></td><td>Read-write</td><td>Zipcode of the tenant.</td></tr><tr><td>state</td><td>&lt;String></td><td>Read-write</td><td>State of the tenant.</td></tr><tr><td>last_name</td><td>&lt;String></td><td>Read-write</td><td>URL of the tenant.</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>city</td><td>&lt;String></td><td>Read-write</td><td>City of the tenant.</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Id of the parent tenant.</td></tr><tr><td>url</td><td>&lt;String></td><td>Read-write</td><td>URL of the tenant.</td></tr><tr><td>address</td><td>&lt;String></td><td>Read-write</td><td>URL of the tenant.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>email_address</td><td>&lt;String></td><td>Read-write</td><td>Email Address of the tenant.</td></tr><tr><td>country</td><td>&lt;String></td><td>Read-write</td><td>Country of the tenant.</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>phone_number</td><td>&lt;String></td><td>Read-write</td><td>Phone number of the tenant.</td></tr><tr><td>preferred_lang</td><td>&lt;String></td><td>Read-write</td><td>Preferred Language.</td></tr><tr><td>first_name</td><td>&lt;String></td><td>Read-write</td><td>First name of the tenant.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



