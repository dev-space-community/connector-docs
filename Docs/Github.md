# GitHub Connector User Documentation

## Overview:
The GitHub Connector is a robust tool designed to seamlessly integrate with your GitHub repositories, making it easy to fetch detailed repository information. By simply providing the necessary inputs, this connector retrieves all relevant data, including issues, pull requests, comments, and more. Whether you're managing open-source projects or private repositories, the GitHub Connector ensures you have quick and organized access to your repository’s data, enabling efficient code management and collaboration using our products **ACE Search and Chat**.

## Create a GitHub PAT (Classic)
1. Navigate to the top-right corner and click on your profile photo.
2. Click on **Settings**.
3. Go to **Developer settings** from the left-hand side panel.
4. Click on **Personal access tokens**, and then **Tokens (classic)**.
5. Click on **Generate new token**, and then select **Generate new token (classic)** from the dropdown.

Please provide the following minimal permissions while generating the token.

![Github](Images/Github1.png)

## User Guide
1. Provide any name for the knowledge.
2. Enter the GitHub token you generated.
3. If the repository falls under any organization, then provide the name of the organization. Otherwise, leave it blank.
4. Enter the desired repository.
5. If the repository is your personal repository and doesn't fall under any organization, then enter the path of the repository eg. "userID/repository_name"

    ![Github](Images/Github2.png)

## Supported entities:

1. Issue title
2. Issue body
3. Issue state
4. Issue url
5. Issue created at
6. Issue updated at
7. Issue closed at
8. Issue user
9. Issue labels
10. Issue assignees
11. Issue milestone
12. Issue comments
13. Issue repository
