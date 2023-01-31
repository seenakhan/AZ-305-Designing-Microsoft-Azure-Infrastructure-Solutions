# Instructions

## Exercise 4: Enable Security Default / Disable Security Defaults

In this exercise you are going to Enable or disable the security defaults. Security defaults make it easier to help protect your organization from identity-related attacks with preconfigured security settings. It enforces the following:

  - Requiring all users to register for Azure AD Multi-Factor Authentication.
  - Requiring administrators to do multifactor authentication.
  - Requiring users to do multifactor authentication when necessary.
  - Blocking legacy authentication protocols.
  - Protecting privileged activities like access to the Azure portal.

In this lab, you will:

+ Task 1: Enable Security Default

### Task 1: Enable Security Default

In this task you are going to enable the security defaults.

#### Pre-requisites for this task

An Azure account with security administrator, Conditional Access administrator, or global administrator privilege.

#### Steps:

1. Go to Azure Active directory.

2. Select **Properties**, then select **Manage Security defaults**.

    ![img](../media/secr1b.png)

3. on the **Enable security defaults** side screen Set the Enable security defaults toggle to **Yes** then select **Save**.

    ![img](../media/secr1.png)

 Now your Security defaults are enabled.
 
4.  Take an **In private window**, enter the link https://www.office.com/?auth=2 and login with the username and password provided in environment details.

You can see there is a message showing **skip for now (14 days until this is required)**. This means all users in your tenant must enroll in multifactor authentication (MFA) via Azure AD Multi-Factor Authentication. Users have 14 days to sign up for Azure AD Multi-Factor Authentication via the Microsoft Authenticator app or any app that supports OATH TOTP. After 14 days, the user is unable to sign in until registration is completed. After enabling security defaults, a user's 14-day period begins after their first successful interactive sign-in.

![img](../media/secr2.png)

5. To disable the Security defaults please repeat step 1 and step 2, then on the **Enable security defaults** side screen Set the Enable security defaults toggle to **No** then select any one of the option listed (here selected **My organization is using Conditional Access**), then select **Save**.

![img](../media/secr3.png)

6. Test again with Office 365 login by taking an **In private window**, enter the link https://www.office.com/?auth=2 and login with the username and password provided in environment details.

![img](../media/secr4.png)

You can see there is no message like **skip for now (14 days until this is required)**

