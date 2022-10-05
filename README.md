**<h1>This WebAPP envisages the use of Amazon EC2 Instances, MySQL Database, Security Groups, and an ElasticIP address.</h1>**

<br>
<h2>The AWS CloudFormation template deploys the following workflows and services:</h2>
<ul>
  <li>The stack deploys an EC2 instance, MySQL Database, Security Groups</li>
  <li>The stack enables interaction with the EC2 instance via the Command Line Interface</li>
  <li>The stack also adopts the use of Elastic IP address.
    <p>An Elastic IP address is a reserved public IP address that you can assign to any EC2 instance in a particular region, until you choose to release it</p>
  </li>
  
</ul>

<br>
<br>

 <h2>Custom Deployment of the CloudFormation Template</h2>
 <ul>
    <li>Clone this Repository</li>
    <li>Set up an AWS account</li>
    <li>Configure AWS CLi with your local credentials file</li>
    <li>Edit the code to fill in peculiar details such as DbName, UserName, MasterPassword, etc.</li>
 </ul>

| Parameter     | Description |
| ----------- | ----------- |
| Profile   | The AWS Credential      |
| Resources | The resources are The EC2 instance, the DB Instance, the RDS Security Group, EIP, and the EC2 Security Group|
| ImageId | It can either be blank (" "), or go to [Amazon EC2 AMI Locator](https://cloud-images.ubuntu.com/locator/ec2/) to pick an AMI ID |
| KeyName | The key name allows users connect to the EC2 instance from the command prompt or thr CLI |
| DbName | The meaning of this parameter differs according to the database engine you use. For MySQL, DBName is the name of the database to create when the DB instance is created |
| MasterUsername | The master user name for the DB instance|
| MasterUserPassword| The password for the master user. The password can include any printable ASCII character except "/", """, or "@"  |
<br>


<p>
Next, use the following command 

<mark>```AWS cloudformation create-stack --stack-name [nameOfStack] --template-body file://iac.yaml```</mark>

 to launch a CloudFormation template to create the the EC2 instance, MySQL DB, Security Groups, EIP. Wait for this template to complete (you can watch progress from the command line or AWS CloudFormation console)
</p>


<h4>Task Lists</h4>
<hr>
<ul>
    <li>Create an AWS Account, IAM User and  Key pair</li>
    <li>Update the CloudFormation Template to reflect your details.</li>
    <li>Where you see '##String', edit accordingly.</li>
</ul>
<br>

You are advised to go through the *[AWS Documentation](https://docs.aws.amazon.com/AWSCloudFormation/latest/UserGuide/aws-resource-rds-dbinstance.html) or (https://docs.aws.amazon.com/)* for detailed explanation on required parameters when deploying DB instance on CloudFormation. </p>
