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
</p>

<p align="center">
Lauching a new EC2 instance:  
<br/>
<img src="images/Screenshot 2024-09-14 at 8.57.19 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br/>
<br/>
</p>

<p align="center">
In the Name and tags section, for Name, type a name that you like, such as: webserver01. In the Application and OS images section, under Quick Start, choose Amazon Linux.
<br/>
<img src="images/Screenshot 2024-09-14 at 8.58.27 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
Clicked the Amazon Machine Image (AMI) dropdown menu & choose Amazon Linux 2 AMI (HVM). For Instance type I choose t2.micro: 
<br/>
<img src="images/Screenshot 2024-09-14 at 9.05.06 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
For Key pair name, choose Proceed without a key pair: 
<br/>
<img src="images/Screenshot 2024-09-14 at 9.17.04 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
For VPC, choose LabVpc.
For Subnet, choose the subnet in the us-east-1a Availability Zone
For Security group name, type: 
Security-Group-Lab
For Description, type: 
HTTP Security Group
For Type, choose HTTP: <br/>
<img src="images/Screenshot 2024-09-14 at 9.20.04 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="images/Screenshot 2024-09-14 at 9.22.51 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
In the Configure storage section, for Root volume, choose gp2 from the dropdown menu.
<br/>
<img src="images/Screenshot 2024-09-14 at 9.28.31 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
This user data script launches a web server, using port 80, to display internal information about the instance. The code block in your file is longer than what is displayed in the screenshot example.
<br/>
<img src="images/Screenshot 2024-09-14 at 9.31.25 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
Upload user data file to automate configuration
<br/>
<img src="images/Screenshot 2024-09-14 at 9.33.01 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
Instance is successfully launched
<br/>
<img src="images/Screenshot 2024-09-14 at 9.36.20 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
Selected “view all instances” to view the instance i just created & copied the IPv4 DNS (ec2-54-86-74-204.compute-1.amazonaws.com) to load this:
<br/>
<img src="images/Screenshot 2024-09-14 at 9.40.37 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="images/Screenshot 2024-09-14 at 9.40.57 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
Launched the 2nd instance from the one I previously made:
<br/>
<img src="images/Screenshot 2024-09-14 at 9.47.59 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<p align="center">
Change the name and subnet associated with this new instance
<br/>
<img src="images/Screenshot 2024-09-14 at 9.48.43 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="images/Screenshot 2024-09-14 at 9.50.25 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
Completed launch of the 2nd EC2 instance and verified that it was up and running.
<br/>
<img src="images/Screenshot 2024-09-14 at 9.51.12 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="images/Screenshot 2024-09-14 at 9.57.18 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="images/Screenshot 2024-09-14 at 9.56.41 PM.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />  
</p>
