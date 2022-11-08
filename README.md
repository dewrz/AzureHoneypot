# AzureHoneypot
<b>We will be creating a virtual machine in Microsoft Azure with no protections so we can monitor attacks from Sentinel for live SIEM training.</b>

1. We need to setup an account on Microsoft Azures portal. Microsoft gives you a free $200.00 credit, so this makes it easy to test and practice on the platform.
<br>
2. Now we will create our virtual machine and create a resource group for our lab. Under the networking tab, you want to go to NIC network security group and click advanced. Here we will delete the default firewall rule and add a custom one with open permissions. After that click "review and create".
<br>
<br>
<a href="https://imgur.com/hAiaLaB"><img src="https://i.imgur.com/hAiaLaB.jpg" title="source: imgur.com" /></a>
<br>
<br>
<a href="https://imgur.com/i2OhT0C"><img src="https://i.imgur.com/i2OhT0C.jpg" title="source: imgur.com" /></a>
<br>
<br>
3. Next we will create a log analytics workspace so we can route logs from the VM to our SIEM. 
<br>
<br>
<a href="https://imgur.com/SXdI6xi"><img src="https://i.imgur.com/SXdI6xi.jpg" title="source: imgur.com" /></a>
<br>
<br>
4. Now we want to go to Microsoft Cloud Defender, go to pricing for our Honeypot and enable servers.
<br>
<br>
<a href="https://imgur.com/NEdTKc9"><img src="https://i.imgur.com/NEdTKc9.jpg" title="source: imgur.com" /></a>
<br>
<br>
8. Next we head over to the log analytics workspace to connect to our VM.
<br>
<br>
<a href="https://imgur.com/gspaBXs"><img src="https://i.imgur.com/gspaBXs.jpg" title="source: imgur.com" /></a>
<br>
<br>
11. Now we head over and set up Sentinel by clicking "Create Microsoft Sentinel" and add your log analytics workspace.
<br>
<br>
13. After that we RDP into the VM and turn off Windows firewall both private/public.
<br>
<br>
15. Finally I head back over to the Log Analytics Workspace and we can see that someone has already began to brute force the machine from IP 80.66.88.213. When checked against a geolocation API the attack is coming from the Central Federal Distric, Russia.
<br>
<br>
<a href="https://imgur.com/ponQQQP"><img src="https://i.imgur.com/ponQQQP.jpg" title="source: imgur.com" /></a>
<br>
<br>
<a href="https://imgur.com/KuNq3oi"><img src="https://i.imgur.com/KuNq3oi.jpg" title="source: imgur.com" /></a>
<br>
<br>
<h3>Lessons Learned:</h3>
Setting up this lab was pretty straight forward with no difficulties, but if someone does set this up, they may want to make sure they shut off their VM honeypot so it doesn't eat up resources.
