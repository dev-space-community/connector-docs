# Confluence User Documentation

## Overview
The Confluence Connector allows you to connect to your Confluence instance and extract data from specific spaces or pages. By entering a few essential details, you can access and retrieve the content you need from your Confluence environment.

## Required Inputs
To use the Confluence Connector, you need to provide the following information:

### 1. Wiki URL
- **Description:** The Wiki URL is the address of your Confluence instance. This URL points to the root of your Confluence site where all spaces and pages are hosted.
- **Where to Find:**
  - You can find this in the address bar of your web browser when you log in to Confluence. It usually looks something like `https://yourcompany.atlassian.net/wiki` or `https://wiki.yourcompany.com`.

### 2. Username
- **Description:** The Username is your Confluence account name that you use to log in. This is required for authentication when connecting to Confluence.
- **Where to Find:**
  - Your Username is the email address or the account name associated with your Confluence profile. You can find it in your Confluence account settings or by checking the account you use to log in.

### 3. API Token
- **Description:** The API Token is a secure key used to authenticate your connection to Confluence. It acts as a password specifically for API access, allowing the connector to retrieve data on your behalf.
- **Where to Find:**
  - You can generate an API Token from your Atlassian account under the API token management section. Visit [https://id.atlassian.com/manage/api-tokens](https://id.atlassian.com/manage/api-tokens) to create and manage your API tokens.

### 4. Fetch Type
- **Description:** The Fetch Type determines what kind of content the Confluence Connector will retrieve. This input is a dropdown with two options:
  - **Spaces:** Fetch all spaces within the Confluence site.
  - **Pages:** Fetch specific pages within a space.
- **How to Use:**
  - Select **Spaces** if you want to retrieve a list of all Confluence spaces.
  - Select **Pages** if you want to retrieve content from specific pages within a space.

## How to Use the Confluence Connector
1. **Enter the Required Inputs:** Input the Wiki URL, Username, API Token, and select the appropriate Fetch Type from the dropdown menu.
2. **Connect to Confluence:** After entering the necessary information, the connector will establish a connection to your Confluence instance.
3. **Extract Data:** Based on the selected Fetch Type, the connector will either retrieve a list of spaces or extract content from specific pages, depending on your selection.
