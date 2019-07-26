# aws-config-s3-encryption-remediation
Sample Cloudformation Template that sets up a Config Rule that checks S3 default server-side encryption is enabled, and a remediation action that enables default AED256 server side encryption if non-compliant.

I put this here as a reference because I found the AWS doco on creating remediation configurations for AWS Config to be a bit sparse and it took me a while to get this working correctly.

To run this, deploy into your account either using the AWS Console or a commane line:

`aws cloudformation deploy --stack-name my-s3-config-rule --template-file ConfigS3Encryption.yml --capabilities CAPABILITY_NAMED_IAM  --profile myprof`

Once deployed your Config rule will be avaialble in the AWS Console. Any buckets that are non-compliant can be remediated by selecting the non-compliant buckets and clicking on Remediate.
