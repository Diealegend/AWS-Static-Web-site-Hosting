<br />


<h2>Part 5:</h2>

<p align="center">
Before we create the main CloudFront distribution , we need to go to the S3 bucket and copy the URL into properties tab, static website hosting section:
 <br/>
<img src="https://i.imgur.com/x5HGiQl.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
Now, create your CloudFront distribution:<br/>
<img src="https://i.imgur.com/NrC9B8Y.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
When you first look in the origin section a drop down panel appears where you can select links to the S3 Buckets. These are incorrectly filled in so paste the Bucket URL instead.: 


 <br/>
<img src="https://i.imgur.com/qz7t5TO.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
Disable the Origin Shield to avoid additional charges. This is what the Origin section configuration should look like:

<br/>
<img src="https://i.imgur.com/LYqGGE8.png" height="80%" width="80%" alt="Static Website"/>

<br />
<br />
In the default cache behavior section the only field to modify here is the Viewer protocol policy, where we choose to Redirect HTTP to HTTPS. All the traffic received in HTTP on port 80 will be redirected to HTTPS on port 443, so all connections made on both ports will be secure. 
<br/>
<img src="https://i.imgur.com/OEh28Fn.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
The next section Price classes  we will use Price class 100. The three types of price classes consist of Price Class 100 (Edge locations from North America and Europe), Price Class 200 (Edge locations North America, Europe, Asia, Middle East and Africa), and Price Class All (all Edge locations). The choice of the Price Class is therefore interesting since fewer Edge locations will be used in places where they cost less (see: https://aws.amazon.com/cloudfront/pricing/).

<br/>
<img src="https://i.imgur.com/X0HjoCc.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
Next you will fill in an alternate domain name (CNAME) by inserting main domain name. In the custom SSL certificate field , select the newly created certificate it will look like this when you are done.(Note: don’t select the Legacy client support unless you want to spend $600 that is unnecessary ) 

<br/>
<img src="https://i.imgur.com/4Cq2eW9.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
Next is the redirect bucket follow the dame steps and copy the S3 URL and paste inside the orgin domain: 
<br/>
<img src="https://i.imgur.com/oJdjqqk.png" height="80%" width="80%" alt="Static Website"/>

<br />
<br />
The Alternate domain name (CNAME) will be the redirect domain:
<br/>
<img src="https://i.imgur.com/itmyyow.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
After the configuration of the redirect distribution is complete you can validate it’s creation. One last configuration will have to do in redirect S3 bucket , Properties tab, static website hosting section, not to copy the URL but change the protocol from HTTP to HTTPS. 
<br/>
<img src="https://i.imgur.com/KONkcU3.png" height="80%" width="80%" alt="Static Website"/>

<br />
<br />
Go back to CloudFront, where you copy the web addresses of your CloudFront distributions (Domain name field) in the navigator search bar, in order to verify that you can access your site through these web addresses:
<br/>
<img src="https://i.imgur.com/L9KcbIC.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
To finalize, head to Route 53 to make changes to the A records, so that the web addresses route traffic to your freshly created Cloudfront distributions: 
<br/>
<img src="https://i.imgur.com/0ylJYJd.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
The record for the main domain name should look like this: 
<br/>
<img src="https://i.imgur.com/poZ4fxL.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
The redirect domain name should look like that:
<br/>
<img src="https://i.imgur.com/5q3APPy.png" height="80%" width="80%" alt="Static Website"/>

<br />
<br />
Checking both the http://navigateproject.link and http://www.navigateproject.link : 
<br/>
<img src="https://i.imgur.com/vAd3mTr.png" height="80%" width="80%" alt="Static Website"/>

<br />
<br />
Now we are down we created a static website in HTTPS on aws.
<br/>


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

