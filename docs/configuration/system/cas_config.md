#cas_config



Configuration for CAS configuration resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>eventHubToken</td><td>&lt;String></td><td>Read-write</td><td>eventHubToken.</td></tr><tr><td>status</td><td>&lt;Integer></td><td>Read-write</td><td>Status updated by Agent after reading configuration.</td></tr><tr><td>turnOnEvent</td><td>&lt;Boolean></td><td>Read-write</td><td>Specifies whether events have to be turned on or not.</td></tr><tr><td>eventHubEndpoint</td><td>&lt;String></td><td>Read-write</td><td>End Point.</td></tr><tr><td>blobToken</td><td>&lt;String></td><td>Read-write</td><td>blobToken.</td></tr><tr><td>blobName</td><td>&lt;String></td><td>Read-write</td><td>The container name of the blob for the tenant. Blob name is same as container name.</td></tr><tr><td>blobAccount</td><td>&lt;String></td><td>Read-write</td><td>Account.</td></tr><tr><td>CustomerId</td><td>&lt;String></td><td>Read-write</td><td>CWC CustomerId.</td></tr><tr><td>agent_id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for agent registered with NMX Cloud..</td></tr><tr><td>expires</td><td>&lt;Double></td><td>Read-write</td><td>Token Expire date.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#all)| [GET (ALL)](#get-all)| [MODIFY](#m)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/cas_config?onerror=&lt;String_value&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{cas_config: {
"eventHubToken":<String_value>,
"blobAccount":<String_value>,
"CustomerId":<String_value>,
"blobName":<String_value>,
"status":<Integer_value>,
"blobToken":<String_value>,
"eventHubEndpoint":<String_value>,
"turnOnEvent":<Boolean_value>,
"agent_id":<String_value>,
"expires":<Double_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "cas_config":[{
"eventHubToken":<String_value>,
"status":<Integer_value>,
"turnOnEvent":<Boolean_value>,
"eventHubEndpoint":<String_value>,
"blobToken":<String_value>,
"blobName":<String_value>,
"blobAccount":<String_value>,
"CustomerId":<String_value>,
"agent_id":<String_value>,
"expires":<Double_value>}]}
```







###get (all)







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/cas_config

<b>HTTP Method:</b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "cas_config":[{
"eventHubToken":<String_value>,
"status":<Integer_value>,
"turnOnEvent":<Boolean_value>,
"eventHubEndpoint":<String_value>,
"blobToken":<String_value>,
"blobName":<String_value>,
"blobAccount":<String_value>,
"CustomerId":<String_value>,
"agent_id":<String_value>,
"expires":<Double_value>}]}
```







###modify







<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/cas_config/agent_id_value&lt;String&gt;

<b>HTTP Method:</b>null

<b>Request Payload: </b>
```
{cas_config:{
"eventHubToken":<String_value>,
"blobAccount":<String_value>,
"CustomerId":<String_value>,
"blobName":<String_value>,
"status":<Integer_value>,
"blobToken":<String_value>,
"eventHubEndpoint":<String_value>,
"turnOnEvent":<Boolean_value>,
"agent_id":<String_value>,
"expires":<Double_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "cas_config":[{
"eventHubToken":<String_value>,
"status":<Integer_value>,
"turnOnEvent":<Boolean_value>,
"eventHubEndpoint":<String_value>,
"blobToken":<String_value>,
"blobName":<String_value>,
"blobAccount":<String_value>,
"CustomerId":<String_value>,
"agent_id":<String_value>,
"expires":<Double_value>}]}
```







