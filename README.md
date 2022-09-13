<h1>AWS Static Website Hosting</h1>

 

<h2>Introduction </h2>
This project will introduce concepts on how to host a static website on AWS. Topics that will be covered consist of :
•	Import a domain name on AWS;
•	Create a hosted zone and manage its DNS records;
•	Create S3 Buckets to host website pages;
•	Configure Route 53 to link the domain name to the website;
•	Create an SSL certificate for the website using AWS Certificate Manager (ACM);
•	Create CloudFront distributions to secure the website in HTTPS.
<img src="https://i.imgur.com/CGWZSws.png" height="80%" width="80%" alt="AWS design"/>

<br />


<h2>Project Needs</h2>

- <b>Money For DNS Name</b> 
- <b>Understanding of S3 and DNS </b>


<h2>Part 1:</h2>

<p align="Left">
To be able to host a website you must have or acquire a domain name by either a Third Party or aws.

It is recommended that you purchase from AWS. If the domain name was acquired by a third party you will have to create a hosted zone and link your domain to it.

Buying Domain Name From AWS:
Go to Route53 then select Register domain in order to register a domain name with AWS:
 <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Select the disk:  <br/>
<img src="https://imgur.com/a/HkvwPmu" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Enter the number of passes: <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Confirm your selection:  <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Wait for process to complete (may take some time):  <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Sanitization complete:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
