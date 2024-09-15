<h5>Directory</h5> 

<b>[Tech Portfolio Home](https://github.com/Jays1115/Jalen-Smith.git)</b>
<b>[AWS Projects](https://github.com/Jays1115/AWS-Projects.git)</b>

# Multi Availibility Zone EC2 Deployment

<h2>Description</h2>
Request: The island's stabilization system is failing and needs increased reliability and availability for its computational modules.
<br><br>
Solution: To increase the reliability and availability of the island's stabilization system, Amazon EC2 instances will be deployed across multiple Availability Zones, ensuring fault tolerance and minimizing downtime in case of localized failures.

<h2>Program walk-through:</h2>

<p align="center">
Navigating to the EC2 Section within AWS and reviewing the selected region, making sure its set to N. Virginia (us-east-1): <br/>
<img src="images/Screenshot 2024-09-14 at 8.52.34 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Lauching a new EC2 instance:  <br/>
<img src="images/Screenshot 2024-09-14 at 8.57.19 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
  
In the Name and tags section, for Name, type a name that you like, such as: webserver01. In the Application and OS images section, under Quick Start, choose Amazon Linux.
  <br/>
<img src="images/Screenshot 2024-09-14 at 8.58.27 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br />
<br />

Reviewing objects in the S3 bucket and renaming the text.html file to fit its function. This file contains the code for the error page, which opens whenever something goes wrong: <br/>
<img src="images/Screenshot 2024-09-14 at 8.58.27 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

Ensuring that “block all public access” is set to “off” so that the static website’s visitors will be able to access the website when its launched:  <br/>
<img src="images/Screenshot 2024-09-13 at 8.29.36 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Reviewing the bucket policy. <br/>
Policy details: <br/>
- This policy allows public access to the S3 bucket. <br/>
- Effect says this policy will Allow access. <br/>
- Principal defines who has access. In this case, * represents anyone. <br/>
- Action defines what users can do to objects in the bucket. In this case, users can only retrieve data with GetObject. <br/>
- Resource specifies that this policy applies to only this bucket. <br/>
<img src="images/Screenshot 2024-09-13 at 8.32.53 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Navigated to the S3 bucket properties section to enable static website hosting:  <br/>
<img src="images/Screenshot 2024-09-13 at 8.37.20 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Static website hosting is enabled:  <br/>
<img src="images/Screenshot 2024-09-13 at 8.42.52 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
Copy & pasted the bucket website endpoint into my internet browser to see if the website has been successfully enabled: 
<img src="image/Screenshot 2024-09-13 at 8.45.19 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
Renaming the S3 object to reflect its function within website:  <br/>
<img src="images/Screenshot 2024-09-13 at 8.48.14 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="images/Screenshot 2024-09-13 at 8.48.34 AM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
