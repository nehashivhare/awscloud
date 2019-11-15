Creating resources in AWS 

Explaination of Lucid chart

As the project requirements described, I used the following components
to build the needed infrastructure:
- AWS Container
- Virtual Private Cloud Container
- Availability Zones: Since the requirements said to have high Availability
for Udagram application. Hence I used two AZs
- Two Private Subnets
- Two Public Subnets
- EC2 instances. Two in each of the private Subnets
- Load Balancer for balancing the load on EC2 instances and do health
checks for them. This is placed in public subnet.
- Internet Gateway: To connect the outside network to my VPC
- NAT Gateway: To translate the public IP addresses to private IP
and send these requests to the EC2 instances in the private subnet
and also to forward the response sent by EC2 instances via the private IP
to public network IP. It just maps priavte to public and public to private
IP addresses.
- Auto Scaling Group: To scale up or down based on the requirements
- Router
- IAM: To authenticate EC2 instance to access the S3 bucket

The bucket is hosted in public, hence the request/response comes and goes
via the internetgateway. It gets routed via the load balancer to the
EC2 instances. The NAT Gateway translates the public IP to private and 
and translates the request back from private IP to the public.



