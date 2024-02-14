# AWS VPC Flow Logs Management

## Overview

This script automates the management of AWS VPC Flow Logs, performing tasks such as deleting existing logs, creating new logs for VPCs, and utilizing AWS Kinesis Data Firehose for log delivery. It also assumes a specified IAM role for cross-account access.

## Prerequisites

Before using this script, ensure the following prerequisites are met:

1. AWS CLI and Python must be installed on the system.
2. AWS CLI must be configured with necessary profiles and permissions.
3. The IAM role specified in the script (`account_role`) must exist and have the required permissions.

## Configuration

### AWS Credentials

1. Set up AWS CLI profiles with necessary credentials.
2. Ensure the profile used in the script (`--profile` argument) has the required IAM permissions.

### Script Configuration

The script uses the following parameters:

- `--profile`: Name of the AWS CLI profile with the necessary permissions.
- `--account`: AWS account number where the VPC Flow Logs will be managed.

## Usage

```bash
python vpc_flow_logs_management.py --profile <AWS_CLI_PROFILE> --account <AWS_ACCOUNT_NUMBER>
```
Replace <AWS_CLI_PROFILE> with the name of the AWS CLI profile, and <AWS_ACCOUNT_NUMBER> with the target AWS account number.

## Important Notes
1. The script assumes the existence of the IAM role (account_role) and may need adjustments if the role name or permissions change.
2. Ensure that the specified S3 bucket (s3_bucket_name) and other resource ARNs are correctly configured.
3. Review and update the script to align with any changes in AWS service names or resource identifiers.
