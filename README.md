<br />


<h2>Part 2:</h2>

<p align="center">
A user accesses a website two different ways by entering the www name of the website (www.navigateproject.link) in the search bar or non-www name of the website navigateproject.link in the search bar. To make this website accessible  by both names is by creating two S3 buckets. The s3 Buckets needed is the main and redirect bucket.
The two S3 buckets , are two choices :

•   Make the www name (www.navigateproject.com) the main address of the website.
•   Make the non-www name (navigateproject.com) the main address of the website.

Create the main S3 bucket which must have the same name as the website you ate hosting:
 <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br />
<br />
Then allow this Bucket to be publicly available on the Internet:<br/>
<img src="https://imgur.com/a/HkvwPmu" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<br />
<br />
The main Bucket is now created, it is time to install the files of your website. To do this, go to your Bucket and click on Upload:
 <br/>
<img src="https://i.imgur.com/nCIbXbg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



<br />
<br />
Move to Permissions to modify the Bucket Policy and Insert the following policy and modify it slightly before validating: <br/>
<img src="https://i.imgur.com/cdFHBiU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br />
<br />
Apply the new bucket policy the pages of the website will now be publicly accessible. It should say publicly accessible: 
 <br/>
<img src="https://i.imgur.com/JL945Ga.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br />
<br />
Activate your static website, and indicate the name of your index (index.html) and error (error.html) documents:  <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br />
<br />
Verify the site is accessible by going back to the Static website hosting section to get the temporary URL of the S3 Bucket: <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>


<br />
<br />
Nextstep is copying the same steps with the redirect bucket.Start by creating the www. Bucket (www.navigateproject.link).   <br/>
<img src="https://i.imgur.com/K71yaM2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>



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
