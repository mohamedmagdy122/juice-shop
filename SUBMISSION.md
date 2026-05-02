# DevSecOps Assignment Submission

## Student: Mohamed Magdy

## Question 2 - Why OIDC is safer than AWS Access Keys

OIDC-based authentication is safer than storing AWS access keys as GitHub secrets for several reasons. First, OIDC uses short-lived tokens that expire after each workflow run, while access keys are long-lived and remain valid until manually rotated or deleted. Second, OIDC tokens are scoped to a specific repository and branch through trust policy conditions, meaning only your exact repo can assume the role, whereas a leaked access key can be used from anywhere. Third, there are no static credentials stored in GitHub secrets that could be exposed through secret scanning, logging, or accidental commits. Fourth, OIDC follows the principle of least privilege more naturally since the IAM role defines exactly what actions are permitted, and the trust policy enforces which workflows can assume it. Finally, OIDC provides better auditability through CloudTrail since each token assumption is tied to a specific GitHub Actions run.

## EC2 Instance Details
- Instance ID: i-0a4323478159adea8
- Public IP: 98.83.161.102

## Repository Links
- Juice Shop Fork: https://github.com/mohamedmagdy122/juice-shop
- ArgoCD GitOps Repo: https://github.com/mohamedmagdy122/argocd-gitops-repo
