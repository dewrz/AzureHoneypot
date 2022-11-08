# AzureHoneypot
<b>We will be creating a virtual machine in Microsoft Azure with no protections so we can monitor attacks from Sentinel for live SIEM training.</b>

1. We need to setup an account on Microsoft Azures portal. Microsoft gives you a free $200.00 credit, so this makes it easy to test and practice on the platform.<br>
2. Now we will create our virtual machine and create a resource group for our lab. Under the networking tab, you want to go to NIC network security group and click advanced. Here we will delete the default firewall rule and add a custom one with open permissions. After that click "review and create".
<br>
3. Next we will create a log analytics workspace so we can route logs from the VM to our SIEM. 
<br>
4. Now we want to go to Microsoft Cloud Defender, go to pricing for our Honeypot and enable servers.
