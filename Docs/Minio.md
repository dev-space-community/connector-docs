# MinIO Connector User Documentation

## Description
The MinIO Connector is designed to interact with MinIO storage. It allows users to authenticate, connect to their bucket, and retrieve file content. The connector supports various file formats and can fetch files either from the root directory or a specified folder. Users can interact with the extracted file content using **ACE Chat and Search**. 

---

## Input Parameters
### Required Parameters
1. **Access Key**
   - Description: The access key for MinIO.
   - Example: `minio-access-key`

2. **Secret Key**
   - Description: The secret key for MinIO.
   - Example: `minio-secret-key`

3. **Bucket Name**
   - Description: The name of the bucket to fetch files from.
   - Example: `my-bucket`

4. **Endpoint URL**
   - Description: The API URL for MinIO (include port).
   - Example: `http://127.0.0.1:9000`

### Optional Parameters
1. **Folder Path**
   - Description: The specific folder to fetch files from. `Leave blank` or use `/` to fetch files only from the `root folder`. Nested files are skipped unless explicitly in the folder.
   - Example: `documents/reports`

2. **Region**
   - Enter region if necessary.
   - Example: `us-east-1` 

---

## Example Input

### Fetching Files from Root Folder

To fetch files from the root folder:
- Access Key: `minio-access-key`
- Secret Key: `minio-secret-key`
- Bucket Name: `my-bucket`
- Endpoint URL: `http://127.0.0.1:9000`
- Folder Path: `/`

### Fetching Files from a Specific Folder

To fetch files from a specific folder:
- Access Key: `minio-access-key`
- Secret Key: `minio-secret-key`
- Bucket Name: `my-bucket`
- Endpoint URL: `http://127.0.0.1:9000`
- Folder Path: `project-data`


### Invalid Folder Example
If the folder path does not exist or is empty, an appropriate error will be raised:
```
Error: The folder 'non-existent-folder' does not exist or is empty.
```

---

## Notes
- Ensure the `endpoint_url` points to the API port of your MinIO deployment (e.g., `9000`) and not the console port (e.g., `9001`).
- If invalid credentials are provided, an appropriate error message will be displayed:
  ```
  Error: Authentication failed. Please check your access key and secret key.
  ```
- Nested files are skipped unless explicitly part of the folder path provided.

---

## Supported Entities
The connector supports the following file formats:

1. **Text Files** (`.txt`)
   - Extracts plain text content.
2. **Word Documents** (`.docx`)
   - Extracts textual content from Word files.
3. **PowerPoint Presentations** (`.pptx`)
   - Extracts slide content.
4. **Excel Spreadsheets** (`.xlsx`, `.xlsm`)
   - Extracts data from sheet cells.
5. **PDF Documents** (`.pdf`)
   - Extracts textual content.

---