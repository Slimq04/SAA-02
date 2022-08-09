# IAM
IAM is a global service, which does not required region setting.
Admin account for the root usage.

IAM policy structure
{
  "Version":"2020-01-02",
  "Id":"S3-Account-Permissions",
  "Statement":[
    {
      "Sid":"1",
      "Effect":"Allow",
      "Principal":{
          "AWS":["arn:aws:iam:123456789012:root"]
      }
      "Action":[
          "s3:GetObject",
          "s3:PutObject"
      ],
      "Resource":["arn:aws:s3:::mybucket/*"]
    },
  ],
}
* still need to figure out what is EFFECT and PRINCIPAL
