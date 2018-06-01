#vip

Configuration for vip configuration resource.


##Properties 
<span>(click to see [Operations](#opera))</span>


<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>protocol</td><td>&lt;String></td><td>Read-write</td><td>Protocol used by vip.</td></tr><tr><td>subnet_id</td><td>&lt;String></td><td>Read-write</td><td>Subnet Id of vip.</td></tr><tr><td>admin_state_up</td><td>&lt;String></td><td>Read-write</td><td>Admin is up or down.</td></tr><tr><td>status</td><td>&lt;String></td><td>Read-write</td><td>status of vip.</td></tr><tr><td>port_id</td><td>&lt;String></td><td>Read-write</td><td>Port Id of requests.</td></tr><tr><td>subnet_gateway_ip</td><td>&lt;String></td><td>Read-write</td><td>Ip of subnet gateway for vip.</td></tr><tr><td>network_type</td><td>&lt;String></td><td>Read-write</td><td>Type of network .</td></tr><tr><td>tenant_id</td><td>&lt;String></td><td>Read-write</td><td>Id of admin tenant..</td></tr><tr><td>subnet_cidr</td><td>&lt;String></td><td>Read-write</td><td>subnet_cidr for vip.</td></tr><tr><td>pool_id</td><td>&lt;String></td><td>Read-write</td><td>Vip belongs to this pool id.</td></tr><tr><td>segmentation_id</td><td>&lt;String></td><td>Read-write</td><td>Segmentation_id of vip.</td></tr><tr><td>connection_limit</td><td>&lt;String></td><td>Read-write</td><td>Maximum number of connections allowed for the vip.</td></tr><tr><td>address</td><td>&lt;String></td><td>Read-write</td><td>Public Ip address of vip from subnet id.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>Id is system generated key for vip.</td></tr><tr><td>loadbalancer_id</td><td>&lt;String></td><td>Read-write</td><td>Id of loadbalancer.</td></tr><tr><td>session_persistence</td><td>&lt;vipsessionpersistence></td><td>Read-write</td><td>Sesssion persistence state of vip.</td></tr><tr><td>name</td><td>&lt;String></td><td>Read-write</td><td>Name of vip.</td></tr><tr><td>protocol_port</td><td>&lt;String></td><td>Read-write</td><td>Port number of protocol.</td></tr><tr><td>diameter</td><td>&lt;String></td><td>Read-write</td><td>Value of diameter protocol.</td></tr><tr><td>description</td><td>&lt;String></td><td>Read-write</td><td>Describes the properties of vip.</td></tr><tr><td>network_id</td><td>&lt;String></td><td>Read-write</td><td>Network_id of vip.</td></tr></tbody></table>
##Operations 
<span>(click to see [Properties](#prope))</span>


[GET (ALL)](#get-)| [GET]()


Some options that you can use for each operations:
<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>



***Note:*** 
Mandatory parameters are marked in <span style="color:#FF0000;">red</span>and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.

###get (all)



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/vip
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "vip":[{"protocol":<String_value>,"subnet_id":<String_value>,"admin_state_up":<String_value>,"status":<String_value>,"port_id":<String_value>,"subnet_gateway_ip":<String_value>,"network_type":<String_value>,"tenant_id":<String_value>,"subnet_cidr":<String_value>,"pool_id":<String_value>,"segmentation_id":<String_value>,"connection_limit":<String_value>,"address":<String_value>,"id":<String_value>,"loadbalancer_id":<String_value>,"session_persistence":<vipsessionpersistence_value>,"name":<String_value>,"protocol_port":<String_value>,"diameter":<String_value>,"description":<String_value>,"network_id":<String_value>}]}```



###get



<b>URL:</b>https://&lt;MGMT-IP&gt;/nitro/v1/config/vip/id_value&lt;String&gt;
<b>HTTP Method:</b>null
<b>Response Payload: </b>```{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "vip":[{"protocol":<String_value>,"subnet_id":<String_value>,"admin_state_up":<String_value>,"status":<String_value>,"port_id":<String_value>,"subnet_gateway_ip":<String_value>,"network_type":<String_value>,"tenant_id":<String_value>,"subnet_cidr":<String_value>,"pool_id":<String_value>,"segmentation_id":<String_value>,"connection_limit":<String_value>,"address":<String_value>,"id":<String_value>,"loadbalancer_id":<String_value>,"session_persistence":<vipsessionpersistence_value>,"name":<String_value>,"protocol_port":<String_value>,"diameter":<String_value>,"description":<String_value>,"network_id":<String_value>}]}```



