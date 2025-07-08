## Creating a Launch Template
1. Navigate to EC2
2. In the left sidebar, under *Instances* click *Launch Templates*
3. Click *Create launch template*
4.Provide a name and description for your template
5.Under *Application and OS Images* select an AMI 
6.Choose an instance type
7.Under *Key pair* select an existing key pair or create a new one
8.Configure security groups to allow necessary traffic
9.Add storage and other configurations as needed
10.Click *Create launch template*

## Creating an Application Load Balancer
1. On the left, under *Load Balancing*, select *Load Balancers*
2. Click *Create Load Balancer*. Under *Application Load Balancer*, click *Create*
3. Give it a name, scheme, and IP Address type
4. Select your VPC and availability zones.
5. Click *Next* to go to security groups.
6. Assign a security group.
7. Click *Next* to go to Listeners and Routing.
8. Configure listener. Create a new target group or use an existing one.
9. Register targets if you need to.
10. Click *Create*


## Creating an Auto Scaling Group
1. Navigate to EC2
2. On the left, click on *Auto Scaling Groups*
3. In the Launch Template section, pick the new launch template you just made.
4. Click *Next*
5. Pick your VPC
6. Pick 2 subnets
7. Attach the load balancer you just made.
8. Click *Next*
9. Configure Group Size and Scaling Policies
10. Add notifications or tags if desired
11. Click *Create Auto Scaling group*

## Validating Funcionality and Testing
1. Add stress to an EC2 instance in your target group so it will go over whichever threshold you specified.
2. Monitor the instance for when it goes over.
3. Check that new instances are being created by ASG.