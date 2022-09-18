<br />


<h2>Part 4:</h2>

<p align="Left">
The next step in this process is for us the create a SSL certificate with aws. First go to AWS Certificate Manager and request a certificate:
<br/>
<img src="https://i.imgur.com/aqlvmK6.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
The certificate will be used on a public website, so you need to request a public certificate: <br/>
<img src="https://i.imgur.com/z3OC0xl.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
Another thing to note is when applying for an SSL cert, you will be asked for Fully Qualified Domain Names (known as FQDN).For this project we have two www.navigateproject.link and navigateproject.link. Fill them both in this same certificate so that the connections by these two addresses are in HTTPS.

For validation method you will want to choose DNS Validation. After that, all you have to do is validate the SSL Certificate creation request: 


 <br/>
<img src="https://i.imgur.com/621sfpW.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
The certificate is created, but not yet validated; let's check its configuration:

<br/>
<img src="https://i.imgur.com/B0l6IkP.png" height="80%" width="80%" alt="Static Website"/>

<br />
<br />
During the configuration of the certifications, you will have to add records of type CNAME in your hosted zone. With AWS it does it automatically all you have to do is click Create records in Route 53: 

<br/>
<img src="https://i.imgur.com/UNBiFil.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
After that Create records in Route 53. All you have to do is wait a few minutes until you see the Success status: 

<br/>
<img src="https://i.imgur.com/B7kACOk.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
It's done, AWS has filled in the CNAME records for you. You can verify it by moving to your hosted zone. These two freshly named CNAME records, allowing you to validate the SSL certificate you just created. Now that the certificate is ready you need to apply it to your website and for that you will need cloud front.

<br/>
<img src="https://i.imgur.com/QXuI08L.png" height="80%" width="80%" alt="Static Website"/>

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


