# packer-aws-example
It is an  example for creating AWS AMIs with packer. 
For more details on packer, visit http://packer.io

This creates an AMI using the AWS builder 

# To Install Packer
URL: https://www.packer.io/docs/installation.html

# Create a x.509 self signed certificate 
And Mention the crt and key file in the json  file

# General Packer Info
To validate a packer template file, run

	packer validate aws.json

This will validate your aws.json file and ready to build.

# Create an AMI (EBS)
Go to aws-ebs-ec2 and validate the packer file:

	packer validate aws.json

The result should be something like this:

	Template validated successfully.

This will build your AMI with packer.this will time as packer creates an instance using the defined source_ami.
  
we need replace the **access key** and your **secret key** that we can find in the Amazon AWS Console.

If your build succeeds, you will get a console output like this:

	Build 'amazon-ebs' finished.
	==> Builds finished. The artifacts of successful builds are:  

	--> amazon-ebs: AMIs were created:
	<instance region>: <source-ami>

we can now use your newly created AMI to create new EC2 instances!
