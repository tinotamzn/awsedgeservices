# CloudFront re:invent 2018 - Builders session

To setup up the labs for this builder session, download the Zip file containing the necessary CloudFormation templates at: http://setup.awsedgeservices.com/cf-reinvent-2018.zip

Unzip the file and you will find a bash script that can be used to deploy the templates.  In order to synthesize the CloudFormation templates for the "Secure your Site - Using CDN Security features to protect your content and infrastructure" builder session, you need the following:

* An AWS account with root credentials (to run 04_signed_url_and_signed_cookies) or an IAM user with administration permissions.
* A linux machine with the AWS credentials for the root account or IAM user configured.
* AWS cli installed (see https://docs.aws.amazon.com/cli/latest/userguide/awscli-install-linux.html).
* If you dont have a linux machine, you can create a new EC2 instance with latest Ubuntu AMI or synthesize all the CloudFormation templates by using the AWS console.

To synthesize the CloudFormation templates, do the following:

**On linux:**

```bash
# NOTE: you can provide --region <REGION> and --profile <AWS_CRED_PROFILE> if needed.
% synthesize.sh
```

**On other OS:**
1. Sign in to the AWS Management Console and open the CloudFormation console at https://console.aws.amazon.com/cloudformation/
1. Click on **Create Stack**
1. Select **Upload a template to Amazon S3** and press **Browse...**
1. Search for **<path>/00_common/cf_reinvent_2018_common.yml** file
1. Click **Next**
1. Use the following configuration:
 * Stack name: **CFReInvent00**
1. Press **Next**, **Next** and **Create**
1. Wait for the stack status to be **CREATE_COMPLETE**
1. Repeat from step 2 for each template in order# awsedgeservices
