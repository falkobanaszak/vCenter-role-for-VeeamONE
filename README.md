# Creating a new vCenter server role with cumulative privileges and permissions to use with Veeam ONE V11

This PowerShell / PowerCLI script lets you create a new vCenter server role with all the cumulative privileges and permissions to use them with Veeam ONE V11.

The privileges used are based on the recommendations out of the Veeam Help Center which you can find here:
[Connection to Virtualization Servers](https://helpcenter.veeam.com/docs/one/deployment/connection_to_virtual_servers.html?ver=110)

Simply execute the script and follow the steps to fill in the relevant data like your vCenter server name, the username and your password. The script will then ask you to choose a name for your new role and automatically creates it.

![Example execution of the script](https://github.com/falkobanaszak/vCenter-role-for-VeeamONE/blob/main/VeeamONE%20PowerCLI%20Role.png)

Feel free to give me feedback on this script, as I want to further improve it.

After you have created the role you need to assign a user to it and continue within VeeamONE where you add your vCenter Server.
![Connecting vCenter Server](https://github.com/falkobanaszak/vCenter-role-for-VeeamONE/blob/main/connecting_vsphere_host_address.png)

**Already planned improvements**
 - [ ] Add a function to assign a user to the role
 - [ ] Add a function to check against an existing role, print the missing privileges and let the user decide to apply the missing privileges to the already existing role

You can get the script here: [New_vCenterRole_VeeamONE.ps1](https://github.com/falkobanaszak/vCenter-role-for-VeeamONE/blob/main/New_vCenterRole_VeeamONE.ps1)

Successful tested against: 
- VMware vCenter 6.5
- VMware vCenter 6.7
- VMware vCenter 7.0
- Veeam ONE V11
