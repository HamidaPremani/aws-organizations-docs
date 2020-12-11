# AWS Compute Optimizer and AWS Organizations<a name="services-that-can-integrate-compute-optimizer"></a>

AWS Compute Optimizer is a service that analyzes the configuration and utilization metrics of your AWS resources\. Resource examples include Amazon Elastic Compute Cloud \(Amazon EC2\) instances and Auto Scaling groups\. Compute Optimizer reports whether your resources are optimal and generates optimization recommendations to reduce the cost and improve the performance of your workloads\. For more information about Compute Optimizer, see the [AWS Compute Optimizer User Guide](https://docs.aws.amazon.com/compute-optimizer/latest/ug/what-is.html)\.

Use the following information to help you to help you integrate AWS Compute Optimizer with AWS Organizations\.

**Topics**
+ [Service\-linked roles created when you enable integration](#integrate-enable-slr-compute-optimizer)
+ [Service principals used by the service\-linked roles](#integrate-enable-svcprin-compute-optimizer)
+ [Enabling trusted access with Compute Optimizer](#integrate-enable-ta-compute-optimizer)
+ [Disabling trusted access with Compute Optimizer](#integrate-disable-ta-compute-optimizer)

## Service\-linked roles created when you enable integration<a name="integrate-enable-slr-compute-optimizer"></a>

The following [service\-linked roles](https://docs.aws.amazon.com/IAM/latest/UserGuide/using-service-linked-roles.html) are automatically created in your organization's accounts when you enable trusted access\. These roles allow Compute Optimizer to perform supported operations within the accounts in your organization\.

You can delete or modify these roles only if you disable trusted access between Compute Optimizer and Organizations or if the account is removed from the organization\.
+ `AWSServiceRoleForComputeOptimizer`

## Service principals used by the service\-linked roles<a name="integrate-enable-svcprin-compute-optimizer"></a>

The service\-linked roles in the previous section can be assumed only by the service principals authorized by the trust relationships defined for the role\. The service\-linked roles used by Compute Optimizer grant access to the following service principals:
+ `compute-optimizer.amazonaws.com`

## Enabling trusted access with Compute Optimizer<a name="integrate-enable-ta-compute-optimizer"></a>

For information about the permissions needed to enable trusted access, see [Permissions required to enable trusted access](orgs_integrate_services.md#orgs_trusted_access_perms)\.

**To enable trusted access using the Compute Optimizer console**  
You must sign in to the Compute Optimizer console using your organization's management account\. Opt\-in on behalf of your organization by following the instructions at [Opting in your Account](https://docs.aws.amazon.com/compute-optimizer/latest/ug/getting-started.html#account-opt-in) in the *AWS Compute Optimizer User Guide*\.

## Disabling trusted access with Compute Optimizer<a name="integrate-disable-ta-compute-optimizer"></a>

For information about the permissions needed to disable trusted access, see [Permissions required to disable trusted access](orgs_integrate_services.md#orgs_trusted_access_disable_perms)\.

On the Organizations side, you can disable trusted access by running a AWS CLI command, or by calling an API operation in one of the AWS SDKs\.

**Important**  
We recommend that where possible, you use the AWS Compute Optimizer console or tools to disable integration with Organizations so that AWS Compute Optimizer can perform any cleanup steps that it requires\. Proceed with these steps only if you can’t disable integration using the other service’s tools\.  
If you are the administrator of only AWS Organizations and not AWS Compute Optimizer, wait until the administrator of AWS Compute Optimizer tells you that they disabled integration with that service’s console or tools, and that any resources have been cleaned up\.

------
#### [ AWS CLI, AWS API ]

**To disable trusted service access using an Organizations AWS CLI command or API**  
You can use the following AWS CLI commands or API operations to disable trusted service access:
+ AWS CLI: [aws organizations disable\-aws\-service\-access](https://docs.aws.amazon.com/cli/latest/reference/organizations/disable-aws-service-access.html)

  You can run the following command to disable AWS Compute Optimizer as a trusted service with Organizations\.

  ```
  $ aws organizations disable-aws-service-access \
      --service-principle compute-optimizer.amazonaws.com
  ```

  This command produces no output when successful\.
+ AWS API: [DisableAWSServiceAccess](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DisableAWSServiceAccess.html)

------