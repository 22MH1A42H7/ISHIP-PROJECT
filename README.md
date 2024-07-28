
# ISHIP-PROJECT
## CONFIGURE A APPLICATION LOAD BALANCER TO THE HIGH-TRAFFIC WEBSITE
### 1.	Login to AWS Management Console


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/1.jpg" width="700" height="400">
</p>


### 2.	Go to the EC2 Dashboard.


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/2.jpg" width="700" height="400">
</p>


### 3.	Lunch an ec2 instance with the name called Project1.


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/3.jpg" width="700" height="400">
</p>


### 4.	Configure your web application on the instance.
<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/4.jpg" width="700" height="400">
</p>

### 5.	Make sure to add the security group rules which is required to web application (HTTP:80, SSH:22).

### 6.	Copy the public ipv4 address and browse on the internet to see the web application working or not.

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/5.jpg" width="700" height="400">
</p>

### 7.	After the Successful deployment, Create the target group.
### 8.	Click on Target Groups in the left-hand menu under Load Balancing.
### 9.	Click Create target group.
<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/6.jpg" width="700" height="400">
</p>


## Configure the target group settings:
### 11.	Give it a name and optionally a description.
### 12.	Choose the target type (e.g., EC2 instances).
### 13.	Configure health checks and protocols according to your application's requirements.

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/7.jpg" width="700" height="400">
</p>



<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/8.jpg" width="700" height="400">
</p>

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/9.jpg" width="700" height="400">
</p>


### 14.	 Click on Create target group.

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/10.jpg" width="700" height="400">
</p>

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/11.jpg" width="700" height="400">
</p>

### 15.	Create an Application Load Balancer (ALB):
### 16.	Click on Load Balancers in the left-hand menu under Load Balancing.
### 17.	Click on Create Load Balancer

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/13.jpg" width="700" height="400">
</p>

### And select the Application Load Balancer.

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/14.jpg" width="700" height="400">
</p>

##	Configure the ALB settings:
### 18.	Give it a name.

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/15.jpg" width="700" height="400">
</p>

### 19.	Select the availability zones where your instances are located.

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/16.jpg" width="700" height="400">
</p>

### 20.	Configure listeners (e.g., HTTP on port 80).
### 21.	Select the target group created in the previous step.
### 22.	Configure security settings (e.g., HTTPS if needed).


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/17.jpg" width="700" height="400">
</p>

### 23.	Create load balancer.

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/18.jpg" width="700" height="400">
</p>

### 26.	After created the load balancer, 

<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/20.jpg" width="700" height="400">
</p>

## 27.Testing:
### •	Once the ALB is created and DNS is updated, test the website to ensure it's accessible via the ALB's DNS name.
### •	Verify that traffic is evenly distributed across your instances.  


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/21.jpg" width="700" height="400">
</p>


### 28.Stop the one instance and Check the Traffic is Going through another instance.


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/22.jpg" width="700" height="400">
</p>


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/23.jpg" width="700" height="400">
</p>


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/24.jpg" width="700" height="400">
</p>

## For the Security Reasons we are making the HTTP protocol of the instance is only go through the SECURITY GROUP of the Load Balancer to secure the outside connections to the IPV4. And now, the Web applications is now only accessable by the only DNS name.

### 29.Going to the instances S-Groups and edit the protocol or inbound roule http source into the S-Group of Load balancer.


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/25.jpg" width="700" height="400">
</p>

### 30.Thats'it! now we can access the website only through the LoadBalancer DNS name only. We cannot access through the instances IPv4, it is way of protection to our instances.


<p align="center">
  <img src="https://github.com/22MH1A05I4/ISHIP-PROJECT/blob/main/JPG'S/26.jpg" width="700" height="400">
</p>
