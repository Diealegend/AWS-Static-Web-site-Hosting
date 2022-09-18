<br />


<h2>Part 3:</h2>

<p align="center">
First, go to Route 53 and look for the DNS records of your hosted zone:
 <br/>
<img src="https://i.imgur.com/RemJkXy.png" height="80%" width="80%" alt="Static Website"/>


<br />
<br />
Note in this screen shot some information may be ahead of your steps.
At your current point  if a user tries to access your website through the main and redirect web addresses, they will have no access and will display that this site can’t be reached.

And what you want is to:
•   Forward the traffic received on the main web address to the main S3 Bucket;
•   Forward the traffic received on the redirect web address to the redirect S3 Bucket.

To correct this task you have to create new DNS records specifically an A record, which allows you to redirect the traffic received to an IPv4 address. In this case, you won't need to specify any IPv4 address, AWS will provide the IP address of the Bucket for you.


For the first DNS Record you want to route traffic from your main web address (in this example navigateproject.com):<br/>
<img src="https://i.imgur.com/2F0xg1u.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
1.  If your main address is www, then add www to the record name. If your main address is non-www, leave the record name as it is;
2.  Select the Record type A to route the traffic to the main S3 Bucket;
3.  Activate the Alias to specify the S3 Bucket to which you want to route the traffic;
4.  Choose an Alias to S3 website endpoint in the region where the Bucket is located (here us-east-1), and select the Bucket that is automatically displayed in the selection;
5.  Routing policy will be simple routing;
6.  No need to evaluate the target health since the website is hosted on S3.

Once the first record is created, wait several minutes before checking if your website is accessible via the main web address

The second DNS record is next
You want to route the traffic of your redirect web address (in this example www.navigateproject.com).

 <br/>
<img src="https://i.imgur.com/yMgIu0F.png" height="80%" width="80%" alt="Static Website"/>



<br />
<br />
1.  If your redirect address is www, then add www to the record name. If your redirect address is non-www, leave the record name as it is;
2.  Select again a Record type in A to route the traffic to the redirect S3 Bucket;
3.  Activate the Alias to specify the S3 Bucket to which you want to route the traffic;
4.  Choose an Alias to S3 website endpoint in the region where the Bucket is located (here us-east-1), and select the Bucket that is automatically displayed in the selection;
5.  Routing policy will be simple routing;
6.  No need to evaluate the target health since the site is hosted on S3.
Once the second record is created, wait again for several minutes before checking if your website is accessible via the web redirect address.Once that happens you should be able to go to your website and be redirected to the main site. However one more problem arises if you look In the URL bar it say Not secure. To fix this we must :
First, create an SSL certificate for your domain by using AWS Certificate Manager (ACM);
Then, use CloudFront to make your site issue HTTPS connections, adding the newly created SSL certificate to your website, and redirecting all HTTP traffic to HTTPS.
After that, your website will be safe and more secure for future users.

It is now time for you to create your first SSL certificate with AWS Certificate Manager.

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
