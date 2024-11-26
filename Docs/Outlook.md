# Outlook Connector User Documentation

## **Overview**
The Outlook Connector is a powerful integration tool designed to connect your Microsoft Outlook account with the platform. It enables seamless extraction of email data for analysis and use in various applications. This connector allows super admins to securely configure essential credentials, while end users can specify their preferences, such as the time range for retrieving emails. Additionally, it supports recurring runs, enabling automated data extraction at defined intervals.

## **Setup Instructions**

### **Credentials Configured by Super Admins**
Super admins are responsible for setting up the following critical credentials to ensure secure and proper integration with Microsoft Outlook:

1. **Client ID**: The unique identifier for your application in the Azure portal, used for authenticating with the Microsoft API.
2. **Client Secret**: A secure key provided by Microsoft, ensuring encrypted communication between the application and the Microsoft server.
3. **Tenant ID**: The unique identifier of your Azure Active Directory instance, required to authenticate and authorize API requests.

Super admins must ensure these credentials are correctly configured for the connector to function properly.


### **Credentials Configured by Users**
Users can customize the connector settings to retrieve specific email data based on their needs:

- **Months**: Specify the number of past months (up to 6 months) from which emails should be fetched. For example, selecting "3" will retrieve emails from the last 3 months.


## **Recurring Runs**
The Outlook Connector supports automated, recurring runs to ensure email data is regularly updated without manual intervention. Users can define the interval for these runs as follows:

1. **Hours**: Set the frequency to run every specified number of hours.
2. **Days**: Schedule the runs to occur daily or every few days.
3. **Months**: Opt for monthly recurring runs to capture new email data over extended periods.

Recurring runs help maintain up-to-date email data, improving efficiency and reliability for ongoing projects.



By combining robust admin-level configuration, user-specific customization, and automated recurring runs, the Outlook Connector offers a seamless and flexible solution for managing email data.


Here’s an example of how the credentials for the Outlook Connector might look:  


## Example Summary:

### **Credentials Configured by Super Admins**
- **Client ID**:  
  `12345abcde-67890fghi-jklmnopqrst-uvwxyz123456`  
  *(A unique identifier for your app registered in Azure AD)*  

- **Client Secret**:  
  `ABCDEF1234567GHIJKLMNOP890`  
  *(A secure key generated in Azure AD for the app registration)*  

- **Tenant ID**:  
  `abcdefgh-1234-5678-ijklmnopqrst`  
  *(The identifier for your organization's Azure Active Directory instance)*  

### **Credentials Configured by Users**
- **Months**:  
  `3`  
  *(Specifies fetching emails from the past 3 months)*  


### **Recurring**
- **Interval**:  
  - **Hours**: Every `6` hours  
  - **Days**: Every `2` days  
  - **Months**: Every `1` month  

## Supported entities:
1. Email subject
2. Email body
3. Sender
4. Received date and time