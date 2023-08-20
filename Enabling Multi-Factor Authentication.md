# Enabling Multi-Factor Authentication using Conditional Access Policy in Azure Active Directory

Multi-factor authentication (MFA) is a security feature of Microsoft Azure Active Directory that requires users to provide two or more verification methods to access a resource. This feature prompts the users for the additional form of identity verification such as something users knows or something users have or something the users are and also can be integrated with (Self Service Password Reset) to reduce IT support requests related to forgotten passwords.

Various methods of verifications are available within Multi-factor authentication. Some of the available methods are listed below:

1. Microsoft Authenticator app
2. Windows Hello for Business
3. FIDO2 security key
4. OATH hardware token (preview)
5. OATH software token
6. SMS
7. Voice call

 In Azure Active Directory (Azure AD), MFA can be enabled using a Conditional Access policy. You can also use Securtiy Defaults to enforce Multi-factor authentication for all users.

There are few prerequisities you need to consider for implementing MFA in your environment. You need to have an Azure AD tenant with administrator access and user accounts or groups that you want to enable MFA for before proceeding ahead with the implementation of MFA within your environment.

## Steps

The steps for the implementation of MFA is outlined below:

1. Log into Azure AD Admin Centre (aad.portal.azure.com) using user account having administrator access.
2. Click on Azure Active Directory.
3. Click on Conditional Access under the Security section.
3. Click on New policy to create a new Conditional Access policy.
4. Give your policy a name.
5. Under Assignments, select Users and groups and choose the users/groups that you want to apply the policy to. You can also exclude specific users, groups or        directory roles.
6. Under Cloud apps or actions, select the cloud app that you want to apply the policy to. You can also exclude selected cloud apps to expempt from the policy.
7. Under Conditions, select the conditions that you want to apply to the policy. For example, you can require MFA if the user is accessing the app from outside of the corporate network. 
8. Under Access controls, select Grant, and then select Grant access and require multi-factor authentication. 
9. Enable the policy to "Report-Only" and click on create. 

These steps will now configure the conditional access policy for Multi Factor Authentication. Test your Conditional Access Policies to only specific subsets of users or groups and verify that the Multi Factor Authentication has been configured successfully. You can then roll out this security feature of Azure AD on a tenant level by enabling the policy in "On" mode.


