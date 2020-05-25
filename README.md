# GitLab_PoC_AWS
AWS CloudFormation Template that builds a GitLab CE PoC Environment

This is intentionally keept super simple and avoids operational concerns like high availability, regional redundancy, backups, etc.  This is meant to be a bare-bones deployment that’s quick to stand up so that the user can get to using GitLab quickly.  A cannot stress enough that this architecture is not designed with working in a production operations capacity.

The design builds two Amazon EC2 instances in a single subnet, in a single VPC, in a single Region.  The first EC2 instance runs Amazon Linux 2, and hosts docker.  The version of GitLab deployed will be the latest build of the Docker CE container on Dockerhub.  The second EC2 instance also uses Amazon Linux 2 as the OS, and serves as the target for vm for deployed software.  This vm runs the GitLab Runner client software.

![AWS Resources Created](https://github.com/nathaniel-avery/GitLab_PoC_AWS/blob/master/GitLab_PoC_in_AWS.png)

## Getting Started
All you need to get started is an AWS Account, basic networking knoweldege, and some prior experience with CloudFormation.

### Installing
Download the CloudFormation YAML file.
Copy the File to an AWS S3 Bucket in your account
Launch CloudFormation from teh console; Point to the CF TEmplate in the right S3 Bucket

## Contributing
I'm always open to suggestions to make things better.

## Authors
Nathaniel Avery - initial version - will add other authors as needed. :)
