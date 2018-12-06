#ns_clusternode



Configuration for ns_clusternode resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>clusterid</td><td>&lt;Integer></td><td>Read-write</td><td>Cluster Instance ID.<br>Minimum value = 1<br>Maximum value =</td></tr><tr><td>nodeid</td><td>&lt;Integer></td><td>Read-write</td><td>Cluster Node ID.<br>Maximum value =</td></tr><tr><td>clnodeip</td><td>&lt;String></td><td>Read-write</td><td>Cluster Node IP.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>password</td><td>&lt;String></td><td>Read-write</td><td>Password of the CCO node(CLIP).<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>iscco</td><td>&lt;Boolean></td><td>Read-write</td><td>Is CCO.</td></tr><tr><td>clip</td><td>&lt;String></td><td>Read-write</td><td>Cluster IP.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>node_group</td><td>&lt;String></td><td>Read-write</td><td>Node Group where the node belongs in L3 Cluster.</td></tr><tr><td>islocalsdx</td><td>&lt;String></td><td>Read-write</td><td>Is Node Belonging to Local SDX.</td></tr><tr><td>clnodehealth</td><td>&lt;String></td><td>Read-only</td><td>Health of the node in the cluster.</td></tr><tr><td>nnmcurconn</td><td>&lt;Double></td><td>Read-only</td><td>Number of Connections open for node to node connection..</td></tr><tr><td>nnmerrmsend</td><td>&lt;Double></td><td>Read-only</td><td>Number of errors in sending node-to-node multicast/broadcast messages.</td></tr><tr><td>nnmtotconntx</td><td>&lt;Double></td><td>Read-only</td><td>Number of node-to-node messages sent.</td></tr><tr><td>act_id</td><td>&lt;String></td><td>Read-only</td><td>Activity Id.</td></tr><tr><td>clnodeeffectivehealth</td><td>&lt;String></td><td>Read-only</td><td>Effective Health of the node in the cluster.</td></tr><tr><td>clptptx</td><td>&lt;Double></td><td>Read-only</td><td>Number of PTP packets transmitted by the node.</td></tr><tr><td>clmasterstate</td><td>&lt;String></td><td>Read-only</td><td>Cluster Master State.</td></tr><tr><td>clsyncstate</td><td>&lt;String></td><td>Read-only</td><td>Sync state of the cluster node.</td></tr><tr><td>cltothbtx</td><td>&lt;Double></td><td>Read-only</td><td>Cluster Number of Heartbeats Sent.</td></tr><tr><td>nnmtotconnrx</td><td>&lt;Double></td><td>Read-only</td><td>Number of node-to-node messages received.</td></tr><tr><td>clptprx</td><td>&lt;Double></td><td>Read-only</td><td>Number of PTP packets received on the node.</td></tr><tr><td>clptpstate</td><td>&lt;String></td><td>Read-only</td><td>PTP state of the node. This state is Master for one node and Slave for the rest.</td></tr><tr><td>cltothbrx</td><td>&lt;Double></td><td>Read-only</td><td>Cluster Number of Heartbeats Received.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





[REMOVE_NODE](#remove)





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note:</b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note:*** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



###remove_node







<b>URL: </b>https://&lt;MGMT-IP&gt;/nitro/v1/config/ns_clusternode?action=remove_node;onerror=&lt;String_value&gt;

<b>HTTP Method: </b>null

<b>Request Payload: </b>
```
{ns_clusternode: {
<b>"nodeid":<Integer_value></b>,
"clusterid":<Integer_value>,
"clnodeip":<String_value>,
"password":<String_value>,
"clip":<String_value>,
"iscco":<Boolean_value>,
"node_group":<String_value>,
"islocalsdx":<String_value>}}
```

<b>Response Payload: </b>
```
{ "errorcode": 0, "message": "Done", "severity": ;ltString_value>, "ns_clusternode":[{
"clnodehealth":<String_value>,
"clusterid":<Integer_value>,
"nodeid":<Integer_value>,
"nnmcurconn":<Double_value>,
"clnodeip":<String_value>,
"nnmerrmsend":<Double_value>,
"nnmtotconntx":<Double_value>,
"password":<String_value>,
"act_id":<String_value>,
"iscco":<Boolean_value>,
"clnodeeffectivehealth":<String_value>,
"clip":<String_value>,
"clptptx":<Double_value>,
"clmasterstate":<String_value>,
"clsyncstate":<String_value>,
"cltothbtx":<Double_value>,
"nnmtotconnrx":<Double_value>,
"clptprx":<Double_value>,
"clptpstate":<String_value>,
"node_group":<String_value>,
"cltothbrx":<Double_value>,
"islocalsdx":<String_value>}]}
```







