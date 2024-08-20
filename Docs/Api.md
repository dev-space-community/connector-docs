# APIConnector User Documentation

## Overview

The `APIConnector` class is a flexible and user-friendly utility designed to facilitate the integration of APIs within our products **ACE Search** and **Chat**. It abstracts the complexities of HTTP requests, authentication, and error handling, allowing users to fetch data from APIs and convert the responses into knowledge objects seamlessly.

## Key Features

- **Automatic Handling of Authentication**: Supports Bearer tokens and Basic Authentication based on provided inputs.
- **Flexible Input Handling**: Safely parses JSON strings for headers and body.
- **Error Handling**: Captures and raises detailed exceptions for common HTTP errors.
- **Integration**: Converts API responses into knowledge objects with relevant metadata.

## User Guide

### Initialization

To create an instance of the `APIConnector` class, you need to provide various parameters that define how the API request should be made. Below is a guide on how to fill out these details.

### Parameters

- **`endpoint`** (str, required):  
  The URL of the API endpoint you want to access.

- **`auth_token`** (str, optional):  
  The authentication token (e.g., Bearer token or custom token). If provided, it will be included in the `Authorization` header of the request.

- **`username`** (str, optional):  
  The username for Basic Authentication. Must be provided together with the `password`.

- **`password`** (str, optional):  
  The password for Basic Authentication. Must be provided together with the `username`.

- **`headers`** (str, optional):  
  HTTP headers to be included in the request. This can be provided as a JSON string or as a dictionary. If you use a JSON string, it will be automatically parsed into a dictionary.

- **`params`** (str, optional):  
  Query parameters for the request. This can be provided as a JSON string or as a dictionary.

- **`body`** (str, optional):  
  The body of the request, typically used for POST requests. This can be provided as a JSON string or as a dictionary.

- **`method`** (str, optional):  
  The HTTP method to use for the request (e.g., GET, POST). The default is `"GET"`.

- **`timeout`** (int, optional):  
  The timeout duration for the request in seconds. If not provided, the request will use the default timeout.

- **`proxies`** (str, optional):  
  Proxy servers to route the request through. This can be provided as a JSON string.

- **`verify`** (str or bool, optional):  
  Whether to verify SSL certificates. This can be provided as a string (`"True"` or `"False"`). The default is `"True"`.

- **`cookies`** (str, optional):  
  Cookies to include in the request. This can be provided as a JSON string or as a dictionary.

### Example Usage

Here’s an example of how you might fill in the parameters:

1. **Endpoint**:  
   `https://api.example.com/data`

2. **Authentication Token**:  
   `auth_token: eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...`

3. **Username**:  
   `username: john_doe`

4. **Password**:  
   `password: secret_password`

5. **Headers**:  
   `headers: {"Content-Type": "application/json"}`

6. **Query Parameters**:  
   `params: {"q": "search_term", "limit": 10}`

7. **Body**:  
   `body: {"data": "ACME vs Databricks?\nNew line here"}`

8. **HTTP Method**:  
   `method: POST`

9. **Timeout**:  
   `timeout: 30`

10. **Proxies**:  
    `proxies: {"http": "http://10.10.1.10:3128", "https": "http://10.10.1.10:1080"}`

11. **SSL Verification**:  
    `verify: False`

12. **Cookies**:  
    `cookies: {"session_id": "abc123"}`


### Conclusion

The `APIConnector` class is designed to streamline the process of making API requests and integrating their responses within the platform products **ACE Search** and **Chat**. By following this user guide, you can easily configure and use the connector to interact with various APIs, regardless of the authentication method or request details.
