# IAM - Identity and Access Management

#### Type: Security
#### Scope: Global
#### Description: Controls access of users to your AWS account services

IAM is a very important service in AWS. It is not made for solve a external problem, instead acting as a "guard" for all other services. As AWS was growing, hundreds and thousands of people has been conecting to a company account to make their work, so it has been seen the necessity to control how much access different users has to accounts.

## Core Concepts

- ### When a AWS account is made, a **root user** is created by default. This user has access to everything, so it is recommended to not use or share it;

- ### You can create many users you want;

- ### Treat a user as a person that will use that login;

- ### You can create **groups** and assign users to them;

- ### Include a strong Password Policy;

    To change the Password Policy, go to ```IAM > Account settings (Sidebar) > Change password policy```

    Some suggestions:

    - Require at least one lowercase, uppercase, number and non-alphanumeric symbols;
    - Require a minimum length of 8;
    - Require users to change their password after X days;
    - Register past passwords to avoid reutilization. 

- ### IAM is all about policies. Each policy represent a rule that all users/groups/services assigned to the policy will follow;

    There it has a bunch of pre-made policies, but you can create you own too.
    
    Generally, policies will be of Read, Write or Full Access. To services communicate to each other, they have to be the right policy. 

    When attaching policies to users, it is a far better idea to create groups then assign users to them and **never** attach the policy directly to the user. This way you have control of the roles that users can have, changing a user role only switching its group instead of looking in the user policies list.

- ### Make use of the MFA and encourage other to use it too

    Multi-factor authentication will add a strong and reliable security to your AWS account.

    You can enable MFA in the main screen of the IAM section.

- ### You can access your AWS user in three ways:

    - AWS Management Console: The web interface
    - AWS CLI: A Command Line Interface to access AWS services in a shell environment
    - AWS SDK: AWS has Software Developer Kit in several programming languages to manage services programatically  

    In the last two, you`ll have to create access keys. To create it, go to ```IAM > Users (Sidebar) > select a user > Create access key```
    It will enable the download of the Access Key ID and Secret. Make sure you download and store wisely because it will not become visible again.

- ### Make use of Credential Report to generate audits about all users activities

    Go to ```IAM > Credential Report (Sidebar) > Download Report``` to access a report of your account.