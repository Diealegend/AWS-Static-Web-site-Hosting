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

<p align="center">
To be able to host a website you must have or acquire a domain name by either a Third Party or aws.

It is recommended that you purchase from AWS. If the domain name was acquired by a third party you will have to create a hosted zone and link your domain to it.

Buying Domain Name From AWS:
Go to Route53 then select Register domain in order to register a domain name with AWS:
 <br/>
<img src="https://i.imgur.com/6J8eZKn.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
Choose the domain name that you want by searching and adding the domain to the cart. (I suggest for projects find the cheapest that’ll fit your needs): <br/>
<img src="https://i.imgur.com/UkN49RX.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
You have to take ownership of your domain(make sure to not use false information).I f you are worried about privacy, it is possible to activate Privacy Protection (also called WHOIS privacy) so that your data will not be visible to any user making WHOIS queries on your domain name. I recommend you activate it. Fill out registrant form: 
<br/>
                                                                         
<img src="https://i.imgur.com/WmmCwkw.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
Then decide if you would like to activate automatic renewal for your domain. If you plan on keeping longer than a year you can enable if not disable it.If disabled you could after expiration use your domain name.  <br/>
<img src="https://i.imgur.com/dliizOR.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
If you purchased a domain name from a third party you will have to create a hosted zone. A hosted zone is a container for records, and records contain information about how you want to route traffic for a specific domain, such as example.com, and its subdomains (acme.example.com, zenith.example.com). A hosted zone and the corresponding domain have the same name.If you created a domain name with amazon you can skip this process.


First, create your hosted zone, where you specify your domain name, in the example cif-project.com; then specify that you want your hosted zone to be public, otherwise it will be inaccessible from the public internet:
 <br/>
<img src="https://i.imgur.com/Iu0wuXS.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
The hosted zone is now created , and contains DNS records of type NS(Name Server) and SOA (Start of Authority): <br/>
<img src="https://i.imgur.com/HRbrUCh.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
Now you need to link your domain name purchased from a third-party domain registrar with your hosted zone. To do this, you will need to map the NS records of your hosted zone to the DNS configuration of the domain purchased from the domain registrar. The DNS configuration of the purchased domain can be easily found in the domain registrar’s dashboard.(CloudisFree-ydamni)

An example will clarify the situation; here is how to do it with the third-party domain registrar, Hostinger:

The two following pictures have been retrieved from this link: https://support.hostinger.com/en/articles/1696789-how-to-change-nameservers-at-hostinger

First of all, go to the dashboard of the domain registrar by connecting to the customer area, then ask to change the DNS servers of the domain name:  <br/>
<img src="https://i.imgur.com/io4xZhR.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
You are redirected to a page, where you specify the names of the DNS servers contained in the NS record of the hosted zone:  <br/>
<img src="https://i.imgur.com/GZjZD3a.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
Insert in these fields the NS records of your hosted zone:  <br/>
<img src="https://i.imgur.com/hXWPQqc.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
Once you are done wait a few minutes before checking the propagation in real time with a dns information search tool . Verify that all the public DNS in the world have the information that your domain name uses the NS of your AWS hosted zone.  <br/>


</p>

<a href="https://github.com/Diealegend/AWS-Static-Web-site-Hosting/blob/8dc049b8beca29e35c6f422be12e823e2bfdf792/README.md/" >Part 2</a>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
