# Instructions

## Exercise 3: Add App Registration for Access via Apps.

In this exercise you are going to register an application with Azure Active Directory, which enables a user with Power Apps user account to connect to their Microsoft Dataverse environment from external client applications using OAuth authentication.

In this lab, you will:

+ Task 1: Create an application registration.

### Task 1: Create an application registration

In this task you are going to create an application registration.

#### Pre-requisites for this task

An Azure account.

#### Steps:

1. In the Azure portal, go to **Active Directory**, then select **App registrations**, then select **+ New registration**.

    ![img](../media/appr1.png)

2. In the **Register an application** page, enter your application's registration information:

    | Section | Values |
    | ------- | ------ |
    | Name | **contosoapp-test** |
    | Supported account types | Select **Accounts in this organizational directory only** |
    | Redirect URI (optional) | Select **Web** and enter **https://contosoapp-test.com** |
    
3. Select **Register** to create the application. 

    ![img](../media/appr2.png)
    
4. On the **Overview** section of **contosoapp-test**, select **Application ID URI**.

    ![img](../media/appr3.png)

5. Select **+ Add scope**.

    ![img](../media/appr4.png)

6. On the **Add a scope** side screen please enter the following information:
  
    | Section | Values |
    | ------- | ------ |
    | Scope name | **scope1** |
    | Who can consent? | Select **Admins and Users** |
    | Admin consent display name | **View user files** |
    | Admin consent description | **Allows app to view theuser details** |
    | State | **Enabled** |
   
    ![img](../media/appr5.png)














