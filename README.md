# AWS Billing Alarm CloudFormation Template

Use this template to set up billing alarms in your AWS account. You will receive billing alarms to your email and your phone number. 

Important: Can only be deployed in `eu-east-1`, since SMS endpoint subscription is only supported in this region.

## Todo:
1. Change email to your email
2. Change phone number to your phone number 
3. Under `Mappings` set appropriate values for thresholds
4. Upload your file and create your stack
   ```
   cloudformation deploy --template template.yaml --capabilities CAPABILITY_IAM
   ```
5. Once the stack is created, go to your email account and verify your email address (you should get an email from SNS)
6. Test if everything works correctly, go to SNS and [publish a message](https://console.aws.amazon.com/sns/v2/home?region=us-east-1#/publish) to your Topic
7. **Under Billing > Billing preferences > Activate Receive Billing Alerts feature**

You should now receive automated billing alarms to your inbox and your phone.

Have fun!

