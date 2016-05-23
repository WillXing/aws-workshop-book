# Module 6 - RDS

1. **Open the URL:**  
[https://ap-southeast-2.console.aws.amazon.com/rds/home?region=ap-southeast-2#dbinstances:](https://ap-southeast-2.console.aws.amazon.com/rds/home?region=ap-southeast-2#dbinstances:)

2. **Click button**: Lauch DB Instance  
3. **On Wizard Step 1: Select Engine**  
    Select: MySQL
4. **On Wizard Step 2: Production?**  
    Select: Dev/Test => MySQL  
5. **On Wizard Step 3: Specify DB Details**  
  
    **DB Instance Class**: db.t2.micro - 1 vCPU, 1GiB RAM  
    **Multi-AZ Deployment**: No  
    **Allocated Storage**: 5 GB  
    **DB Instance Identifier**: awsworkshoprds  
      
    **Master Username**: rdsadmin  
    **Master Password**: rdspassword  
    **Confirm Password**: rdspassword 
      
    Set other fields to default
6. **On Wizard Step 4: Configure Advanced Settings**  

    **VPC Security Group(s)**: default(VPC)  
    **Database Port**: 3306
    
    Set other fields to default  
      
    **Then Click button**: Lauch DB Instance
  
7. **Go to RDS Instances page, waiting for the new instance with status = available:**    
[https://ap-southeast-2.console.aws.amazon.com/rds/home?region=ap-southeast-2#dbinstances:](https://ap-southeast-2.console.aws.amazon.com/rds/home?region=ap-southeast-2#dbinstances:)

8. **Check the connection information of the instnace:**  
    **Endpoint**: awsworkshoprds.aws_generated_string.ap-southeast-2.rds.amazonaws.com  
    **Port**: 3306

    ***Note**: Please replace the aws_generated_string with actual string returned 
      
9. Connect to MySQL Instance using parameters described in Step 6 and Step 8  

    ***Note**: Tool 'Sequel Pro' can be found at [http://www.sequelpro.com/](http://www.sequelpro.com/)  
    
    <font color=red>You may not be able to connect to the RDS, please check the Security Group if it is allow the TCP port of the 3306  </font>
     

10. Execute SQL to the connected MySQL DB:
    ```
    SELECT COUNT(*) FROM information_schema.TABLES
    ```
    Possible Results:
    ```
    COUNT(*)
    235
    ```