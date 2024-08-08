# JIRA Connector User Documentation

## 1. Server URL
The server URL is the base URL of your Jira instance. 

- **Jira Cloud:** It typically looks like `https://your-domain.atlassian.net`.
- **Self-hosted Jira:** It will be the URL of your Jira server.

## 2. Username
Your username is usually your email address that you use to log in to Jira.

## 3. API Token

### For Jira Cloud:
1. Go to the [Atlassian API Token](https://id.atlassian.com/manage-profile/security/api-tokens) page.
2. Click on **Create API token**.
3. Give the token a label and click **Create**.
4. Copy the generated token.

### For Self-hosted Jira:
You might need to use your password or a token generated by your administrator, depending on your Jira server's authentication settings.

## 4. Project Key
The project key is a unique identifier for your Jira project. You can find it in the following ways:

- When viewing a project in Jira, the project key is displayed in the project details.
- It's also visible in the URL when you're viewing the project in your browser. For example, in `https://your-domain.atlassian.net/jira/software/c/projects/PROJECTKEY/boards/1`, `PROJECTKEY` is your project key.

## Example Summary

- **Server URL:** `https://your-domain.atlassian.net`
- **Username:** `your-email@example.com`
- **API Token:** Generated from the Atlassian API token page.
- **Project Key:** Visible in the project details or URL in Jira.