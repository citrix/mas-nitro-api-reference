#kubernetes_param



Configuration for Kubernetes params used in triton config resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>client_key</td><td>&lt;String></td><td>Read-write</td><td>Path to the Client key for client certificate based authentication.</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>ca_data</td><td>&lt;String></td><td>Read-write</td><td>CA certificate data (plain or 64base encoded).</td></tr><tr><td>ca</td><td>&lt;String></td><td>Read-write</td><td>Path to the CA certificate.</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>username</td><td>&lt;String></td><td>Read-write</td><td>User to be used for basic authentication.</td></tr><tr><td>client_cert_data</td><td>&lt;String></td><td>Read-write</td><td>Client certificate data for client certificate based authentication (plain or 64base encoded) .</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>User's Password for basic authentication.</td></tr><tr><td>insecure_skip_verify</td><td>&lt;Boolean></td><td>Read-write</td><td>Whether to skip verifying server certificate.</td></tr><tr><td>client_cert</td><td>&lt;String></td><td>Read-write</td><td>Path to the Client certificate for client certificate based authentication.</td></tr><tr><td>token</td><td>&lt;String></td><td>Read-write</td><td>Token for bearer tokens based authentication.</td></tr><tr><td>kubeconfig</td><td>&lt;String></td><td>Read-write</td><td>Path to the kubeconfig file to be used for kubernetes configuration.</td></tr><tr><td>apiserver</td><td>&lt;String></td><td>Read-write</td><td>URL to be used to connect to API server.</td></tr><tr><td>client_key_data</td><td>&lt;String></td><td>Read-write</td><td>Client key data for client certificate based authentication (plain or 64base encoded).</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



