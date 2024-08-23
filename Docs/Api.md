# API connector User Documentation

## Overview

The `API Connector` is a flexible and user-friendly utility designed to facilitate the integration of APIs within our products **ACE Search** and **Chat**. It abstracts the complexities of HTTP requests, authentication, and error handling, allowing users to fetch data from APIs and convert the responses into knowledge objects seamlessly.

## Key Features

- **Automatic Handling of Authentication**: Supports Bearer tokens and Basic Authentication based on provided inputs.
- **Flexible Input Handling**: Safely parses JSON strings for headers and body.
- **Error Handling**: Captures and raises detailed exceptions for common HTTP errors.
- **Integration**: Converts API responses into knowledge objects with relevant metadata.

## User Guide

### Initialization

To create an instance of the `APIConnector` class, you need to provide various parameters that define how the API request should be made. Below is a guide on how to fill out these details.

### Parameters

- **Endpoint** (str, required):  
  The URL of the API endpoint you want to access.

- **Authentication Token** (str, optional):  
  The authentication token (e.g., Bearer token or custom token). If provided, it will be included in the `Authorization` header of the request.

- **Username** (str, optional):  
  The username for Basic Authentication. Must be provided together with the `password`.

- **Password** (str, optional):  
  The password for Basic Authentication. Must be provided together with the `username`.

- **Headers** (str, optional):  
  HTTP headers to be included in the request. This can be provided as a JSON string or as a dictionary. If you use a JSON string, it will be automatically parsed into a dictionary.

- **Params** (str, optional):  
  Query parameters for the request. This can be provided as a JSON string or as a dictionary.

- **Body** (str, optional):  
  The body of the request, typically used for POST requests. This can be provided as a JSON string or as a dictionary.

- **Method** (drop-down selection, required):  
  The HTTP method to use for the request (e.g., GET, POST). The default is `GET`.

- **Timeout** (int, optional):  
  The timeout duration for the request in seconds. If not provided, the request will use the default timeout.

- **Proxies** (str, optional):  
  Proxy servers to route the request through. This can be provided as a JSON string.

- **Verify** (str, optional):  
  Whether to verify SSL certificates. This can be provided as a string (`True` or `False`).

- **Cookies** (str, optional):  
  Cookies to include in the request. This can be provided as a JSON string or as a dictionary.

### Example Usage

> **Note:**
> 1. Please use double quotes inside a dictionary format, see `Headers`, `Body` etc below.
> 2. Please fill up only necessary API parameters and leave other parameters blank. 

Here’s an example of how you might fill in the parameters:

1. **Endpoint**:  
  `https://api.example.com/data`

2. **Authentication Token**:  
  `eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9...`

3. **Username**:  
  `john_doe`

4. **Password**:  
   `sk-12dts23`

5. **Headers**:  
   `{"Content-Type": "application/json"}`

6. **Parameters**:  
   `{"q": "search_term", "limit": 10}`

7. **Body**:  
   `{"data": "What is AI?"}`

8. **Method**:  
   `POST`

9. **Timeout**:  
   `timeout: 30`

10. **Proxies**:  
    `{"http": "http://10.10.1.10:3128", "https": "http://10.10.1.10:1080"}`

11. **SSL Verification/Verify**:  
    `False`

12. **Cookies**:  
    `{"session_id": "abc123"}`


### Conclusion:

The `API Connector` is designed to streamline the process of making API requests and integrating their responses within the platform products **ACE Search** and **Chat**. By following this user guide, you can easily configure and use the connector to interact with various APIs, regardless of the authentication method or request details.
