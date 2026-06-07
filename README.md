# aws-project-4

# IAM Security Audit Project

Name : Siggari Naga Teja

code tech intern id : CITS802

## Overview

This project performs an IAM Security Audit in AWS to identify security risks, review IAM configurations, and ensure compliance with security best practices.

The audit includes analysis of IAM users, groups, roles, policies, MFA status, access keys, and password policies.

## Project Details

- **Project Name:** IAM Security Audit
- **AWS Account Audit Scope:** IAM Resources
- **S3 Bucket Used:** `new-aws-static-project4`

## Audit Checks Performed

- Review IAM Users
- Review IAM Groups
- Review IAM Roles
- Analyze Attached Policies
- Check MFA Enablement
- Review Access Key Status
- Identify Unused Credentials
- Verify Password Policy
- Detect Overly Permissive Permissions
- Generate Security Findings Report

## Architecture

```text
AWS Account
     |
     |
 IAM Resources
     |
+--------------------+
| IAM Users          |
| IAM Groups         |
| IAM Roles          |
| IAM Policies       |
+--------------------+
     |
     |
 Security Audit
     |
     |
Audit Reports
     |
     |
S3 Bucket
(new-aws-static-project4)
```

## Prerequisites

- AWS Account
- AWS CLI Configured
- IAM Read Permissions
- Access to S3 Bucket
- Python/Boto3 (if using automation scripts)

## Audit Process

### 1. Collect IAM Information

Review:

- Users
- Groups
- Roles
- Policies
- Access Keys
- MFA Status

### 2. Analyze Security Risks

Identify:

- Inactive users
- Unused access keys
- Missing MFA
- Excessive permissions
- Policy misconfigurations

### 3. Generate Audit Report

Security findings are documented and stored for review.

### 4. Upload Report to S3

Audit reports are uploaded to:

```text
s3://new-aws-static-project4
```

## Sample AWS CLI Commands

List IAM Users:

```bash
aws iam list-users
```

List IAM Roles:

```bash
aws iam list-roles
```

Get Account Password Policy:

```bash
aws iam get-account-password-policy
```

List Access Keys:

```bash
aws iam list-access-keys --user-name USERNAME
```

## Expected Outcomes

- Improved IAM Security Posture
- Identification of Security Risks
- Compliance Validation
- Enhanced Access Control
- Security Audit Documentation

## Project Structure

```text
.
├── audit-scripts/
├── reports/
├── screenshots/
├── README.md
```

## Security Best Practices

- Enable MFA for all users
- Rotate access keys regularly
- Apply least privilege access
- Remove unused credentials
- Review IAM policies periodically
- Monitor IAM activity using CloudTrail

## License

This project is licensed under the MIT License.
