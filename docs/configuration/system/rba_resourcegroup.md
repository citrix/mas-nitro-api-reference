#rba_resourcegroup



Configuration for RBA Resource Group resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Tenant Id of the RBA resource group.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>props</td><td>&lt;rba_resourcegroup_props[]></td><td>Read-write</td><td>RBA Resource Group Props.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Resource Group Name.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for RBA resource group.</td></tr><tr><td>roles</td><td>&lt;String[]></td><td>Read-write</td><td>Roles to which this resourcegroup is assigned.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[ADD](#add)| [DELETE](#delete)| [GET (ALL)](#get-all)| [GET](#get)| [UPDATE](#update)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###add







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_resourcegroup?onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{rba_resourcegroup: {
<b>"name":<String_value></b>,
"id":<String_value>,
"roles":<String_value[]>,
"props":[{
<b>"id":<String_value></b>,
"propvalue":<String_value>,
"parent_id":<String_value>,
"propname":<String_value>,
"resourcetype":<String_value>,
"parent_name":<String_value>,
"rbaoperator":<String_value>}],
"tenant_id":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_resourcegroup":[{
"tenant_id":<String_value>,
"props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"resourcetype":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>}],
"name":<String_value>,
"id":<String_value>,
"tenant_name":<String_value>,
"roles":<String_value>}]}
```







###delete







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_resourcegroup/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value> }
```







###get (all)







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_resourcegroup

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_resourcegroup":[{
"tenant_id":<String_value>,
"props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"resourcetype":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>}],
"name":<String_value>,
"id":<String_value>,
"tenant_name":<String_value>,
"roles":<String_value>}]}
```







###get







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_resourcegroup/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_resourcegroup":[{
"tenant_id":<String_value>,
"props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"resourcetype":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>}],
"name":<String_value>,
"id":<String_value>,
"tenant_name":<String_value>,
"roles":<String_value>}]}
```







###update







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/rba_resourcegroup/id_value&lt;String&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{rba_resourcegroup:{
<b>"id":<String_value></b>,
"roles":<String_value[]>,
"name":<String_value>,
"props":[{
<b>"id":<String_value></b>,
"propvalue":<String_value>,
"parent_id":<String_value>,
"propname":<String_value>,
"resourcetype":<String_value>,
"parent_name":<String_value>,
"rbaoperator":<String_value>}],
"tenant_id":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "rba_resourcegroup":[{
"tenant_id":<String_value>,
"props":[{
"parent_name":<String_value>,
"propname":<String_value>,
"resourcetype":<String_value>,
"rbaoperator":<String_value>,
"id":<String_value>,
"parent_id":<String_value>,
"propvalue":<String_value>}],
"name":<String_value>,
"id":<String_value>,
"tenant_name":<String_value>,
"roles":<String_value>}]}
```







