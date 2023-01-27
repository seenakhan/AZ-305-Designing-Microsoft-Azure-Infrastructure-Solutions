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

![img](../media/nuse4.png)

1. In the new user page please enter the following settings (leave others with their defaults) and select **Save**.

    | Setting | Value |
    | --- | --- |
    | User name | **az305-01a-aaduser1** |
    | Name | **az305-01a-aaduser1** |
    | Let me create the password | enabled |
    | Initial password | **Provide a secure password** |
    | Usage location | **United States** |
    | Job title | **Cloud Administrator** |
    | Department | **IT** |

    >**Note**: **Copy to clipboard** the full **User Principal Name** (user name plus domain). You will need it later in this task.

1. Refresh the users page you can see the newly created user named **az305-01a-aaduser1** click on it.

1. In the **Manage** section, click **Assigned roles**, then click **+ Add assignment** button.

![img](../media/nuse5.png)

1. On the **Directory roles** side screen, please search for **User Administratoe** role and select the role, then select **Add**.

![img](../media/nuse6.png)

1. Keep refresh **Assigned roles** page , you can see the **User Administrator** role added successfully.

![img](../media/nuse7.png)

1. Open an **InPrivate** browser window and sign in to the [Azure portal](https://portal.azure.com) using the newly created user account. When prompted to update the password, change the password to a secure password of your choosing. 

    >**Note**: Rather than typing the user name (including the domain name), you can paste the content of Clipboard.

1. In the **InPrivate** browser window, in the Azure portal, search for and select **Azure Active Directory**.

    >**Note**: While this user account can access the Azure Active Directory tenant, it does not have any access to Azure resources. This is expected, since such access would need to be granted explicitly by using Azure Role-Based Access Control. 

1. In the **InPrivate** browser window, on the Azure AD blade, in the **Manage** section, click **Users**, and then click **+ New user**.

![img](../media/nuse8.png)

1. Create a new user with the following settings (leave others with their defaults):

    | Setting | Value |
    | --- | --- |
    | User name | **az305-01a-aaduser2** |
    | Name | **az305-01a-aaduser2** |
    | Let me create the password | enabled |
    | Initial password | **Provide a secure password** |
    | Usage location | **United States** |
    | Job title | **System Administrator** |
    | Department | **IT** |

1. You have successfully created the new user.

![img](../media/nuse9.png)

1. Sign out as the az305-01a-aaduser1 user from the Azure portal and close the InPrivate browser window.


