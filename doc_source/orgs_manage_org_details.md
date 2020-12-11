# Viewing details about your organization<a name="orgs_manage_org_details"></a>

You can perform the following tasks to view details about elements of your organization\.

**Topics**
+ [Viewing details of an organization from the management account](#orgs_view_org)
+ [Viewing details of a root](#orgs_view_root)
+ [Viewing details of an OU](#orgs_view_ou)
+ [Viewing details of an account](#orgs_view_account)
+ [Viewing details of a policy](#orgs_view_policy)

## Viewing details of an organization from the management account<a name="orgs_view_org"></a>

**Minimum permissions**  
To view the details of an organization, you must have the following permission:  
`organizations:DescribeOrganization`

------
#### [ AWS Management Console ]

**To view details of an organization**

When signed in to the organization's management account \(formerly known as the "master account"\) in the [AWS Organizations console](https://console.aws.amazon.com/organizations/), you can view details of the organization\.

1. Sign in to the Organizations console at [https://console\.aws\.amazon\.com/organizations/](https://console.aws.amazon.com/organizations/)\. You must sign in as an IAM user, assume an IAM role, or sign in as the root user \([not recommended](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials)\) in the organization's management account\.

1. Choose the **Settings** tab\.

   The console displays details about the organization, including its ID and the email address of the owner of its management account\.

------
#### [ AWS CLI, AWS API ]

**To view details of an organization**  
You can use one of the following commands to view details of an organization:
+ AWS CLI: [aws organizations describe\-organization](https://docs.aws.amazon.com/cli/latest/reference/organizations/describe-organization.html) 
+ AWS API: [DescribeOrganization](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeOrganization.html)

------

## Viewing details of a root<a name="orgs_view_root"></a>

**Minimum permissions**  
To view the details of a root, you must have the following permissions:  
`organizations:DescribeOrganization` \(console only\)
`organizations:ListRoots` 

------
#### [ AWS Management Console ]<a name="view_details_root"></a>

**To view details of a root**

When signed in to the organization's management account in the [AWS Organizations console](https://console.aws.amazon.com/organizations/), you can view details of a root\.

1. Sign in to the Organizations console at [https://console\.aws\.amazon\.com/organizations/](https://console.aws.amazon.com/organizations/)\. You must sign in as an IAM user, assume an IAM role, or sign in as the root user \([not recommended](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials)\) in the organization's management account\.

1. Choose the **Organize accounts** tab, and then choose **Home**\.

1. Choose the **Root** entity\. Root is the default name, but you can rename it using the API or command line tools\.

   The **Root** pane on the right side of the page shows the details of the root\.

------
#### [ AWS CLI, AWS API ]

**To view details of a root**  
You can use one of the following commands to view details of a root: 
+ AWS CLI: [aws organizations list\-roots](https://docs.aws.amazon.com/cli/latest/reference/organizations/list-roots.html) 
+ AWS API: [ListRoots](https://docs.aws.amazon.com/organizations/latest/APIReference/API_ListRoots.html)

------

## Viewing details of an OU<a name="orgs_view_ou"></a>

**Minimum permissions**  
To view the details of an organizational unit \(OU\), you must have the following permissions:  
`organizations:DescribeOrganizationalUnit`
`organizations:DescribeOrganization` \(console only\)
`organizations:ListOrganizationsUnitsForParent` \(console only\)
`organizations:ListRoots` \(console only\)

------
#### [ AWS Management Console ]<a name="view_details_ou"></a>

**To view details of an OU**

When signed in to the organization's management account in the [AWS Organizations console](https://console.aws.amazon.com/organizations/), you can view details of the OUs in your organization\.

1. Sign in to the Organizations console at [https://console\.aws\.amazon\.com/organizations/](https://console.aws.amazon.com/organizations/)\. You must sign in as an IAM user, assume an IAM role, or sign in as the root user \([not recommended](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials)\) in the organization's management account\.

1. On the **Organize accounts** tab, navigate to the OU that you want to examine\. If the OU that you want is a child of another OU, choose each OU in the hierarchy to find the one you're looking for\.

1. Select the check box for the OU\. 

   The Details pane on the right side of the page shows information about the OU\.

------
#### [ AWS CLI, AWS API ]

**To view details of an OU**  
You can use one of the following commands to view details of an OU:
+ AWS CLI: [aws organizations describe\-organizational\-unit](https://docs.aws.amazon.com/cli/latest/reference/organizations/describe-organizational-unit.html) 
+ AWS API: [DescribeOrganizationalUnit](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeOrganizationalUnit.html)

------

## Viewing details of an account<a name="orgs_view_account"></a>

**Minimum permissions**  
To view the details of an AWS account, you must have the following permissions:  
`organizations:DescribeAccount`
`organizations:DescribeOrganization` \(console only\)
`organizations:ListAccounts` \(console only\)

------
#### [ AWS Management Console ]<a name="view_details_account"></a>

**To view details of an AWS account**

When signed in to the organization's management account in the [AWS Organizations console](https://console.aws.amazon.com/organizations/), you can view details about your accounts\.

1. Sign in to the Organizations console at [https://console\.aws\.amazon\.com/organizations/](https://console.aws.amazon.com/organizations/)\. You must sign in as an IAM user, assume an IAM role, or sign in as the root user \([not recommended](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials)\) in the organization's management account\.

1. Do one of the following:
   + On the **Accounts** tab, choose the account that you want to examine\.
   + On the **Organize accounts** tab, navigate to and then choose an account card\.

   The **Account summary** pane on the right side of the page shows details of the selected account\.

**Note**  
By default, failed account creation requests are available for 90 days and hidden on the **Accounts** tab\. To view a list that includes failed account creation requests, choose the switch at the top to change it to **Show**\.

------
#### [  ]

**To view details of an account**  
You can use one of the following commands to view details of an account:
+ AWS CLI: [aws organizations describe\-account](https://docs.aws.amazon.com/cli/latest/reference/organizations/describe-account.html) 
+ AWS API: [DescribeAccount](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribeAccount.html)

------

## Viewing details of a policy<a name="orgs_view_policy"></a>

**Minimum permissions**  
To view the details of a policy, you must have the following permissions:  
`organizations:DescribePolicy`
`organizations:ListPolicies`

------
#### [ AWS Management Console ]<a name="view_details_policy"></a>

**To view details of a policy**

When signed in to the organization's management account in the [AWS Organizations console](https://console.aws.amazon.com/organizations/), you can view details about your policies\.

1. Sign in to the Organizations console at [https://console\.aws\.amazon\.com/organizations/](https://console.aws.amazon.com/organizations/)\. You must sign in as an IAM user, assume an IAM role, or sign in as the root user \([not recommended](https://docs.aws.amazon.com/IAM/latest/UserGuide/best-practices.html#lock-away-credentials)\) in the organization's management account\.

1. On the **Policies** tab, choose the policy that you want to examine\.

1. Choose **View policy details** in the pane on the right side of the page\.

------
#### [ AWS CLI, AWS API ]

**To view details of a policy**  
You can use one of the following commands to view details of a policy:
+ AWS CLI: [aws organizations describe\-policy](https://docs.aws.amazon.com/cli/latest/reference/organizations/describe-policy.html)
+ AWS API: [DescribePolicy](https://docs.aws.amazon.com/organizations/latest/APIReference/API_DescribePolicy.html)

------