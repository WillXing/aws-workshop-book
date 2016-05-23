# Module 2 - CloudFormation

1. **Prepare a local file with name EC2.template, and copy the below content into it**
```
{
  "AWSTemplateFormatVersion" : "2010-09-09",
    "Description" : "Ec2 block device mapping",
    "Resources" : {
      "MyEC2Instance" : {
        "Type" : "AWS::EC2::Instance",
        "Properties" : {
          "InstanceType" : "t2.micro",
          "ImageId" : "ami-f2210191",
          "KeyName" : "mypaire",
          "BlockDeviceMappings" : [
            {
              "DeviceName" : "/dev/xvda",
                "Ebs" : {
                  "VolumeType" : "gp2",
                  "DeleteOnTermination" : "false",
                  "VolumeSize" : "8"
                }
            },
            {
              "DeviceName" : "/dev/sdk",
              "NoDevice" : {}
            }
          ]
        }
    }
  }
}
```

2. **Open the URL: **  
[https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-2](https://console.aws.amazon.com/cloudformation/home?region=ap-southeast-2)

3. **Create the button 'Create stack'**
4. **On the Wizard:**  
  **4.1. Select Template:**  
    Choose a template -> Upload a template to Amazon S3  

    Specify the file EC2.template saved in Step 1  
  **4.2. Specify Details**  
    Stack name: myawsworkshopstack  
  **4.3. Options **  
    Key: Name  
    Value: awsworkshopec2  
  **4.4. Review**  
    Click button: Create  
5. **Then go to EC2 Instances page, check the instance is being created:**  
[https://ap-southeast-2.console.aws.amazon.com/ec2/v2/home?region=ap-southeast-2#Instances:sort=instanceId](https://ap-southeast-2.console.aws.amazon.com/ec2/v2/home?region=ap-southeast-2#Instances:sort=instanceId)
