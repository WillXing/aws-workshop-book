# Module 3 - ELB

---
* **Prerequisite Check**: Two EC2 instances are available, like set in Module 1 and Module 2   
  **For example**:  
  a). [http://ec2_ip1/app/index.html](http://ec2_ip1/app/index.html)  
  b). [http://ec2_ip2/app/index.html](http://ec2_ip2/app/index.html)  

---

1. **Open page 'Load Balancers' via URL:**  
[https://ap-southeast-2.console.aws.amazon.com/ec2/v2/home?region=ap-southeast-2#LoadBalancers:](https://ap-southeast-2.console.aws.amazon.com/ec2/v2/home?region=ap-southeast-2#LoadBalancers:)

2. **Click button 'Create Load Balancer'**  

3. **One Wizard Step 1: Define Load Balancer**  

  **Load Balancer name**: awsworkshopelb  
  
  Set other fields to default
  
4. **One Wizard Step 2: Assign Security Groups**   
  
  Select default Security Group  
  
5. **One Wizard Step 3: Define Load Balancer**  
  
  Bypass this step  
  
6. **One Wizard Step 4: Define Load Balancer**  
  
  **Ping Protocol**: http  
  **Ping port**: 80
  **Ping path**: /app/index.html
  
  Set other fields to default
  
7. **One Wizard Step 5: Add EC2 Instances**  
  
  Select the two EC2 Instances deccribed in Step 1
 
8. **One Wizard Step 6: Add Tags**  
  
  **Key**: Name  
  **Value**: awsworkshop

9. **One Wizard Step 7: Review**  
  
  Click the button: Create
  
10. **Try the ELB connection**  
  
  **Suppose the returned ELB DNS name is**:   
  awsworkshopelb-1111111111.ap-southeast-2.elb.amazonaws.com  
  
  **Then try the URL**:  
  [http://awsworkshopelb-1111111111.ap-southeast-2.elb.amazonaws.com/sample/index.html](http://awsworkshopelb-1111111111.ap-southeast-2.elb.amazonaws.com/sample/index.html)
  
  Your will get the same returned page as in Step 1
  
  <font color=red>You may not be able to connect to the ELB, please check the Security Group if it is allow the HTTP on port 80  </font>
    