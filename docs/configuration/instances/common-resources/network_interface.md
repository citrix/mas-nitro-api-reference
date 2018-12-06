#network_interface



Configuration for VM device network interface resource.

<span>(click to see [Operations](#operations))</span>



##Properties 

<span>(click to see [Operations](#operations))</span>





<table><thead><tr><th>Name</th><th>Data Type</th><th>Permissions</th><th>Description</th></tr></thead><tbody><tr><td>is_mgmt_ifc</td><td>&lt;Boolean></td><td>Read-write</td><td>True if this is the management interface.</td></tr><tr><td>name_server</td><td>&lt;String></td><td>Read-write</td><td>Name Server.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>vrid_list_ipv6</td><td>&lt;String></td><td>Read-write</td><td>VRID List for Interface/Channel for IPV6 VMAC Generation.</td></tr><tr><td>gateway</td><td>&lt;String></td><td>Read-write</td><td>gateway.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>parent_id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>vrid_list_ipv4</td><td>&lt;String></td><td>Read-write</td><td>VRID List for Interface/Channel for IPV4 VMAC Generation.</td></tr><tr><td>is_member_ifc</td><td>&lt;Boolean></td><td>Read-write</td><td>True if this interface is member of a channel.</td></tr><tr><td>mac_address</td><td>&lt;String></td><td>Read-write</td><td>Mac Address.<br>Minimum length = 1<br>Maximum length = 32</td></tr><tr><td>l2_enabled</td><td>&lt;Boolean></td><td>Read-write</td><td>L2 mode status of Interface.</td></tr><tr><td>id</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>ip_address</td><td>&lt;String></td><td>Read-write</td><td>IP Address.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>netmask</td><td>&lt;String></td><td>Read-write</td><td>netmask.<br>Minimum length = 1<br>Maximum length = 64</td></tr><tr><td>port_name</td><td>&lt;String></td><td>Read-write</td><td>Port name of the interface on the host machine.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>parent_name</td><td>&lt;String></td><td>Read-write</td><td>.</td></tr><tr><td>mac_mode</td><td>&lt;String></td><td>Read-write</td><td>Mac Mode, default for XenServer generated, generated for SVM generated, custom for User assigned.<br>Minimum length = 1<br>Maximum length = 255</td></tr><tr><td>managed_device_id</td><td>&lt;String></td><td>Read-write</td><td>managed_device_id.</td></tr><tr><td>vlan</td><td>&lt;Integer></td><td>Read-write</td><td>This property is not supported.Use vlan_whitelist for vlan configuration;ltbr;gtVLAN Id.<br>Maximum value =</td></tr><tr><td>receiveuntagged</td><td>&lt;Boolean></td><td>Read-write</td><td>Receive Untagged Packets on Interface/Channel.</td></tr><tr><td>sdx_formation_network_id</td><td>&lt;String></td><td>Read-write</td><td>This property is deprecated;ltbr;gtSDX Formation Network Id of which this Interface is part of.<br>Minimum length = 1<br>Maximum length = 128</td></tr><tr><td>vlan_whitelist</td><td>&lt;String></td><td>Read-write</td><td>VLAN Whitelist for Interface/Channel on VM Instance.</td></tr><tr><td>interface_name</td><td>&lt;String></td><td>Read-write</td><td>Name of this interface.</td></tr><tr><td>vrid_list_ipv4_array</td><td>&lt;String[]></td><td>Read-write</td><td>VRID List for Interface for IPV4 VMAC Generation.</td></tr><tr><td>vrid_list_ipv6_array</td><td>&lt;String[]></td><td>Read-write</td><td>VRID List for Interface for IPV6 VMAC Generation.</td></tr><tr><td>vlan_whitelist_array</td><td>&lt;String[]></td><td>Read-write</td><td>VLAN Whitelist for Interface on VM Instance.</td></tr><tr><td>is_vlan_applied</td><td>&lt;Boolean></td><td>Read-write</td><td>Is VLAN added on NetworkInterface of VM Instance.</td></tr><tr><td>device_channel_name</td><td>&lt;String></td><td>Read-only</td><td>LA Name on the actual VM.</td></tr><tr><td>xen_vf_index</td><td>&lt;Integer></td><td>Read-only</td><td>Index given by Xen when assigning free virtual function.</td></tr></tbody></table>

##Operations 

<span>(click to see [Properties](#properties))</span>





Some options that you can use for each operations:

<ul><li><p><b>Getting warnings in response:</b>NITRO allows you to get warnings in an operation by specifying the "warning" query parameter as "yes". For example, to get warnings while connecting to the NetScaler appliance, the URL is as follows:</p><p>http://<span style="color:green;font-style:italic;">&lt;netscaler-ip-address&gt;</span>/nitro/v1/config/login?warning=yes</p><p>If any, the warnings are displayed in the response payload with the HTTP code "209 X-NITRO-WARNING".</p></li><li><p><b>Authenticated access for individual NITRO operations:</b>NITRO allows you to logon to the NetScaler appliance to perform individual operations. You can use this option instead of creating a NITRO session (using the login object) and then using that session to perform all operations,</p><p>To do this, you must specify the username and password in the request header of the NITRO request as follows:</p><p>X-NITRO-USER:<span style="color:green;font-style:italic;">&lt;username&gt;</span></p><p>X-NITRO-PASS:<span style="color:green;font-style:italic;">&lt;password&gt;</span></p><p><b>Note: </b>In such cases, make sure that the request header DOES not include the following:</p><p>Cookie:NITRO_AUTH_TOKEN=<span style="color:green;font-style:italic;">&lt;tokenvalue&gt;</span></p></li></ul>







***Note: *** 

Mandatory parameters are marked in <span style="color:#FF0000;">red</span> and placeholder content is marked in <span style="color:green;font-style:italic">&lt;green&gt;</span>.



