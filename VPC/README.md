VPC Troubleshooting Meetup  

Your goals are to successfully demonstrate the following:  
* That you can ssh into the launched EC2 instance and get a prompt  .
* That the [apache test website](https://cloudbutton-meetups.s3-us-west-2.amazonaws.com/EC2/apache_success.png) is available to the outside world.

What you need to do:  
* Launch either the beginner, intermediate, or advanced stack below. 
* Once the stack is launched with all associated resources:
* Navigate to the Output tab of the NESTED cloudformation stack.  Click on the the DNS Value to launch that in a browser.  This is the URL that needs to respond with the Apache test page to complete that portion of the exercise.
* Begin troubleshooting and make whatever changes are necessary to the resources to achieve the above two goals.

Notes:  
WHEN LAUNCHING THESE VIA THE AWS CLOUDFORMATION CONSOLE USING THE BUTTONS PROVIDED BELOW:  
Under 'Stack Creation Options', consider putting a timeout in of 12 minutes.  That will accelerate any troubleshooting if you run into problems.  
You must check the two boxes on the last screen before launching the stack:  
I acknowledge that AWS CloudFormation might create IAM resources with custom names.  
I acknowledge that AWS CloudFormation might require the following capability: CAPABILITY_AUTO_EXPAND  


|Module          | QuickLaunch |
|----------------|--------------|
|Benchmark| [![Launch Benchmark](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=vpc-meetup-benchmark&templateURL=https://cloudbutton-meetups.s3-us-west-2.amazonaws.com/VPC/CloudFormation/vpc_subnets_create_meetup-benchmark.yaml)|
|Beginner| [![Launch Benchmark](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=vpc-meetup-beginner&templateURL=https://cloudbutton-meetups.s3-us-west-2.amazonaws.com/VPC/CloudFormation/vpc_subnets_create_meetup-beginner.yaml)|
|Intermediate| [![Launch Benchmark](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=vpc-meetup-intermediate&templateURL=https://cloudbutton-meetups.s3-us-west-2.amazonaws.com/VPC/CloudFormation/vpc_subnets_create_meetup-intermediate.yaml)|
|Advanced| [![Launch Benchmark](https://s3.amazonaws.com/cloudformation-examples/cloudformation-launch-stack.png)](https://console.aws.amazon.com/cloudformation/home?region=us-west-2#/stacks/new?stackName=vpc-meetup-advanced&templateURL=https://cloudbutton-meetups.s3-us-west-2.amazonaws.com/VPC/CloudFormation/vpc_subnets_create_meetup-advanced.yaml)|


Reference Architecture

![Reference Architecture](https://cloudbutton-meetups.s3-us-west-2.amazonaws.com/RefArch/RefArch-VPCMeetup.jpeg)


FAQS:  
What version of EC2 is being launched?  
All modules are using launching a fairly recent version of the AWS provided base image of Amazon Linux 2: https://aws.amazon.com/marketplace/pp/B07PWHGXQG
  
Should I launch the benchmark stack?  
No.  This is the 'correct' answer and is here as a reference.  But do not launch this one.  That's cheating.

When I launch the stack, do the parameters matter?  
No. To ensure a smooth launch, do not modify the default parameters.  That will not impact the troubleshooting process

Can I view the template code?  
You could, but it will be more challenging and more 'real-world' troubleshooting if you dive into the environment to troubleshoot.  It's up to you.

Can I diff different templates?  
No.  Again...cheating.  Don't do that. To get the most out of this workshop, you should treat each template as a separate exercise.

Can I launch more than one stack at a time?  
Yes.  The templates are configured so you can launch all of them at once.  Although I suggest doing one at a time.

If I figure out the beginner module, will that make it easier to figure out the intermediate or advanced ones?  
Probably not.  Each module is designed with different variations of incorrect or wrong configuration.

How do I delete the stacks?  
For most of the modules, when you delete the cloudformation stack, it will cleanly delete all the resources.  However, likely one of them will need some manual follow up.  
Instructions for this will follow at the end of the workshop.  Plan for some mop-up.

