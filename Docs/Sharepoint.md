# SharePoint User Documentation

## Overview
The SharePoint Connector allows you to seamlessly connect to your SharePoint site and extract file contents from specified directories. By providing a few key pieces of information, you can access and retrieve data from your SharePoint environment directly to use it into our products **ACE Search and Chat**..

## Required Inputs
To use the SharePoint Connector, you need to provide the following information:

### 1. Tenant Name
- **Description:** The Tenant Name refers to your organization's unique identifier in the Microsoft 365 ecosystem. It is usually a subdomain of onmicrosoft.com or a custom domain name associated with your organization.
- **Where to Find:**
  - You can typically find this in the admin center of Microsoft 365 or Azure Active Directory. It’s often the first part of your SharePoint URLs.
  - Go to your Azure portal (https://portal.azure.com/), search for “Azure AD B2C” in the search tab. Under the Essentials tab, copy the Domain Name. That is your Tenant Name.
  - **Example:** yourcompany.onmicrosoft.com

### 2. Site URL
- **Description:** The Site URL is the specific address of the SharePoint site from which you want to extract file contents. It points to the root of the site collection or a specific sub-site.
- **Where to Find:**
  - This can be found in the address bar of your web browser when you navigate to the desired SharePoint site. It usually looks something like https://yourcompany.sharepoint.com/sites/yoursite.

### 3. Authority URL & Client ID
- **Description:** The Authority URL is the URL used for authentication with Azure Active Directory (AAD). This URL is essential for authorizing the SharePoint Connector to access your resources. The Client ID is a unique identifier for the application you have registered in Azure AD. This ID tells Azure which application is requesting access to SharePoint resources.
- **Where to Find:**
  - Go to your Azure portal (https://portal.azure.com/), and search for “App Registrations” in the search tab. Click on the **New Registration** button to create a new App Registration.
    1. Enter an identifiable name for the application.
    2. Under supported account types, choose **Single tenant**.
    3. Click **Register**.
  - Under the Essentials tab, copy the Application (client) ID. This is your **Client ID**.
  - Under the Essentials tab, copy the Directory (tenant) ID. This is your **Tenant ID**.
  - The Authority URL is typically in the format `https://login.microsoftonline.com/<Tenant-ID>` or `https://login.microsoftonline.com/<Tenant-Name>`. You can get this from the Azure portal under the Azure AD overview page.

### 4. Client Secret
- **Description:** The Client Secret is a secure key that acts as a password for your application. It is used in conjunction with the Client ID to authenticate the application against Azure AD.
- **Where to Find:**
  - You can generate a Client Secret in the Azure portal under **App registrations** -> **Certificates & secrets**. Make sure to copy this key when it’s created, as it will be shown only once.

### 5. Remote Directory
- **Description:** The Remote Directory specifies the folder within the SharePoint site from which you want to extract files. This can be a path to a specific document library or sub-folder within the site.
- **Where to Find:**
  - Navigate to the desired folder in your SharePoint site and note the path. The path usually follows the Site URL, like `/Shared Documents/FolderName`.

## Setting up API Permissions
On the left-hand navigation menu under **Manage**, open **API Permissions**. There are two options for API Permissions. Choose any one:

### 1. Full Privilege API (Easier – API has access to all sites)
- Select the **Add a Permission** button.
- Choose **Microsoft Graph** -> **Application Permission** -> **Sites.ReadWrite.All**.
- Click on **Add Permissions** to save.
- Once the API permissions are added, an Admin User must authorize the API permissions using the **Grant admin consent** button.

### 2. Restricted API (Harder – API has access to only the designated sites)
- Select the **Add a Permission** button.
- Choose **Microsoft Graph** -> **Application Permission** -> **Sites.Selected**.
- Click on **Add Permissions** to save.
- Once the API permissions are added, an Admin User must authorize the API permissions using the **Grant admin consent** button.

### To Grant the API Access to Sites
Call the Microsoft SharePoint API using an authenticated token as shown below:

```bash
curl --location 'https://<SITE_URL>/permissions' \
--header 'Content-Type: application/json' \
--header 'Authorization: Bearer <MICROSOFT_AUTH_TOKEN>' \
--data '{
    "roles": ["write"],
    "grantedToIdentities": [{
        "application": {
            "id": "<CLIENT_ID>",
            "displayName": "<APPLICATION_NAME>"
            }
        }]
}'
```

## How to Use the SharePoint Connector
1.	**Enter the Required Inputs**: Input the Tenant Name, Site URL, Authority URL, Client ID, Client Secret, and Remote Directory into the SharePoint Connector interface.
2.	**Connect to SharePoint**: Once all the required information is provided, the connector will establish a connection to your SharePoint site.
3.	**Extract File Contents**: After successfully connecting, the connector will retrieve the contents of the specified remote directory, allowing you to access and manipulate the files as needed.
