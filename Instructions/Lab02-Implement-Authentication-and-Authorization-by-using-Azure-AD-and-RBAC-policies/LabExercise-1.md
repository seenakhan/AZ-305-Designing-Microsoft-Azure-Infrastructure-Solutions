# Instructions

## Exercise 1: Add a user and provide the accessibility of the resources.

In order to allow Contoso users to authenticate by using Azure AD, you have been tasked with provisioning users and group accounts. Membership of the groups should be updated automatically based on the user job titles. 

In this lab, you will:

+ Task 1: Create and configure Azure AD users
+ Task 2: Create Azure AD groups with assigned and dynamic membership
+ Task 3: Manage Azure AD guest users (Optional - lab environment issue)

### Task 1: Create and configure Azure Active Directory users

In this task you are going to create and configure Azure Active DIrectory users.

#### Pre-requisites for this task

An Azure account 

#### Steps:
1. Sign in to the [Azure portal](https://portal.azure.com).

1. In the Azure portal, Go to **All Services** and select **Azure Active Directory**.

   ![img](../media/use1.png)

1. On the Azure Active Directory blade, scroll down to the **Manage** section, click **User settings**, and review available configuration options.

   ![img](../media/nuse1.png)

1. On the Azure Active Directory blade, in the **Manage** section, click **Users**, and then click your user account to display its **Profile** settings. 

   ![img](../media/nuse2.png)

1. Click **Edit properties**, in the **Settings** section, and check the usage location is UNited States, if not set **Usage location** to **United States** and click **Save** to apply the change.

   ![img](../media/nuse3.png)

    >**Note**: This is necessary in order to assign an Azure AD Premium P2 license to your user account later in this lab.

1. Go back to the **Users - All users** blade, and then click **+ New user**.

1. Create a new user with the following settings (leave others with their defaults):

    | Setting | Value |
    | --- | --- |
    | User name | **az104-01a-aaduser1** |
    | Name | **az305-01a-aaduser1** |
    | Let me create the password | enabled |
    | Initial password | **Provide a secure password** |
    | Usage location | **United States** |
    | Job title | **Cloud Administrator** |
    | Department | **IT** |

    >**Note**: **Copy to clipboard** the full **User Principal Name** (user name plus domain). You will need it later in this task.
