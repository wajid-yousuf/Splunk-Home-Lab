# Splunk-Home-Lab
We will set-up a Splunk home lab, we will learn to install and configure tools required to make a functional and practical Splunk Lab.

**Setting up the Lab Environment**\
We need to have at least two VM's for this lab purpose. I have Ubuntu VM acting as Splunk indexer and windows OS as the endpoint, and send logs generated from Windows OS to Splunk indexer to parse and analyze the logs, and learn pattern-matching and learn to indicate/recognize IoC's.\
In the VirtualBox Menu click on Network -> NAT Networks, click on Create, rename it if you want to. Then type in an IP range click Apply.\
<img width="800" height="659" alt="image" src="https://github.com/user-attachments/assets/e6e1e92f-ba80-46d7-b715-62be3fd6b4fd" />\
In the main VirtualBox menu, right-click on a VM, click on Settings -> Network, select NAT Network
<img width="924" height="544" alt="image" src="https://github.com/user-attachments/assets/9ed24935-e234-484f-a1f5-d92e4be303bf" />


**Download Required Tools**
