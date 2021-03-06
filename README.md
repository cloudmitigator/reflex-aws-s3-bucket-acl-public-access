# reflex-aws-s3-bucket-acl-public-access
A Reflex rule for detecting when a bucket has ACL rules that grant public access.

To learn more about S3 Bucket ACLs, see [the AWS Documentation](https://docs.aws.amazon.com/AmazonS3/latest/dev/S3_ACLs_UsingACLs.html).

## Getting Started
To get started using Reflex, check out [the Reflex Documentation](https://docs.cloudmitigator.com/).

## Usage
To use this rule either add it to your `reflex.yaml` configuration file:  
```
rules:
  aws:
    - s3-bucket-acl-public-access:
        version: latest
```

or add it directly to your Terraform:  
```
module "s3-bucket-acl-public-access" {
  source            = "git::https://github.com/reflexivesecurity/reflex-aws-s3-bucket-acl-public-access.git?ref=latest"
  sns_topic_arn     = module.central-sns-topic.arn
  reflex_kms_key_id = module.reflex-kms-key.key_id
}
```

Note: The `sns_topic_arn` and `reflex_kms_key_id` example values shown here assume you generated resources with `reflex build`. If you are using the Terraform on its own you need to provide your own valid values.

## Configuration
This rule has no configuration options.

## Contributing
If you are interested in contributing, please review [our contribution guide](https://docs.cloudmitigator.com/about/contributing.html).

## License
This Reflex rule is made available under the MPL 2.0 license. For more information view the [LICENSE](https://github.com/reflexivesecurity/reflex-aws-s3-bucket-acl-public-access/blob/master/LICENSE) 
