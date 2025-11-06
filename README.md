# Splunk-Home-Lab
We will set-up a Splunk home lab, we will learn to install and configure tools required to make a functional and practical Splunk Lab.

**Setting up the Lab Environment**\
We need to have at least two VM's for this lab purpose. I have Ubuntu VM acting as Splunk indexer and windows OS as the endpoint, and send logs generated from Windows OS to Splunk indexer to parse and analyze the logs, and learn pattern-matching and learn to indicate/recognize IoC's.\
In the VirtualBox Menu click on Network -> NAT Networks, click on Create, rename it if you want to. Then type in an IP range click Apply.\
<img width="800" height="659" alt="image" src="https://github.com/user-attachments/assets/e6e1e92f-ba80-46d7-b715-62be3fd6b4fd" />\
In the main VirtualBox menu, right-click on a VM, click on Settings -> Network, select NAT Network for both VM's.\
<img width="800" height="659" alt="image" src="https://github.com/user-attachments/assets/9ed24935-e234-484f-a1f5-d92e4be303bf" />\
Open splunk indexer on Linux: Click on Settings->Forwarding & receiving, then in Receive data, click on Add new, set port to 9997 then click Save.\
<img width="800" height="177" alt="two" src="https://github.com/user-attachments/assets/c8585528-d792-4e7f-8416-8551a237f491" />\
<img width="800" height="352" alt="three" src="https://github.com/user-attachments/assets/1924962d-0e3e-4725-952a-f7e1c3e215a0" />\
Then on Windows Os: To install Splunk Universal Forwarder, right-click Install, tick the License Agreement, we can choose to install UF to our desired location by clicking on Customzie Options.\
<img width="494" height="384" alt="four" src="https://github.com/user-attachments/assets/212961aa-9ead-4d27-9bba-68f3540b0baa" />\
Choose the folder where you want to install Splunk Universal Forwarder:\
<img width="490" height="379" alt="five" src="https://github.com/user-attachments/assets/96da264b-080e-4472-a338-f76d17695616" />\
To skip click 'Next':\
<img width="487" height="383" alt="six" src="https://github.com/user-attachments/assets/cc562b97-0ada-4f58-9ec8-1e86bb588531" />\
For now Choose "Local System:"\
<img width="492" height="385" alt="seven" src="https://github.com/user-attachments/assets/6db9ecc9-417e-4104-8faf-cc68d47df242" />\
Click on the logs you want to sent over to Splunk indexer:\
<img width="493" height="383" alt="eight" src="https://github.com/user-attachments/assets/c918ad42-71bc-4cc5-8a29-22878b73d241" />\
Click Next:\
Enter a username and click on Generate Random Password:\
<img width="491" height="391" alt="ten" src="https://github.com/user-attachments/assets/9f6d93ba-addc-4fbc-8a05-a21827a396bf" />\
Now enter the IP address of the workstation or server where you want to send the logs and events or in our case IP address of Ubuntu which has Splunk indexer installed, enter port number 8089.\
<img width="495" height="385" alt="eleven" src="https://github.com/user-attachments/assets/88b16238-ff77-4ade-9c83-77d6f5b13efc" />\
For this one enter the same IP address as above and port number 9997. We can change it later.\
<img width="494" height="384" alt="thirteen" src="https://github.com/user-attachments/assets/220de6af-7868-4f69-8eeb-f0109507bc4f" />\
After that click on "Install".\
<img width="491" height="384" alt="fifteen" src="https://github.com/user-attachments/assets/57731277-024f-470d-80b9-8b23f44222f5" />\
We need to allow outbound connections/ports on Windows Firewall Settings. Click on New Rule.\
<img width="800" height="601" alt="image" src="https://github.com/user-attachments/assets/ad41c11d-b43b-4bec-91b7-b72d27361e9c" />\
Click on Port. Then click Next.\
<img width="708" height="578" alt="seventeen" src="https://github.com/user-attachments/assets/2f07cd8a-8b75-4e96-81eb-4982014a8dc7" />\
In Protocol and Ports, select TCP protocol, type in 8080 and 9997 ports.\
Allow connection in next menu.\
<img width="707" height="574" alt="nineteen" src="https://github.com/user-attachments/assets/bde560b8-3744-4297-afbf-662016911477" />\
Type-in a name for your rule. Click Finish.\
<img width="706" height="575" alt="twenty" src="https://github.com/user-attachments/assets/dff87217-6352-480b-bd0a-4016b867ad3d" />\
 Now on Ubuntu VM, start the Splunk idexer: ```sudo /opt/splunk/bin/splunk start```\
After typing-in the 'http://127.0.0.1:8000', then click on Search & Reporting, and click on Data Summary Tab.\
<img width="796" height="243" alt="twentyone" src="https://github.com/user-attachments/assets/5591e1f2-77be-4a22-8a6a-f3883690667a" />\
<img width="800" height="313" alt="twentytwo" src="https://github.com/user-attachments/assets/ed91a849-a609-405e-87cf-381ee30245f1" />



