# File Connector User Documentation

## Overview:
The File Connector is a versatile tool designed to seamlessly integrate document files into your knowledge base, making it easy to index and retrieve information from various file formats. By simply uploading your documents, this connector processes and organizes all relevant content, enabling efficient information retrieval and management. Whether you're working with PDFs, Word documents, presentations, or text files, the File Connector ensures you have quick and organized access to your document data, enabling efficient knowledge management and collaboration using our products **ACE Search and Chat**.

## User Guide

1. **Navigate to File Connector**
   - Go to the **Files** section in the platform
   - Click on the **Add File Source** tab

2. **Provide Knowledge Name**
   - Enter a descriptive name for your knowledge source in the **Knowledge Name** field (required)
   - Choose a name that clearly identifies the type or purpose of the documents being uploaded

3. **Upload Documents**
   - **Option 1**: Drag and drop your document files into the upload area
   - **Option 2**: Click on **Browse** to select files from your local system
   

4. **Select Resources**
   - Click on the **Resources** dropdown menu (required)
   - Select an appropriate resource allocation option based on your requirements

5. **Manage Group Permissions (Optional)**
   - Click on **+ Add Group Permission** button
   - Configure access controls to specify which groups can use this file source

6. **Save Configuration**
   - Click the **Save** button to create and activate the file source
   - Click **Cancel** to discard changes and exit without saving


## Supported File Formats:

The File Connector supports a wide range of document formats:

1. **PDF** (.pdf) - Portable Document Format
2. **Word Documents** (.doc, .docx) - Microsoft Word files
3. **Text Files** (.txt) - Plain text documents
4. **Markdown** (.md) - Markdown formatted files
5. **PowerPoint** (.ppt, .pptx) - Microsoft PowerPoint presentations
6. **JSON** (.json) - JavaScript Object Notation files
7. **XML** (.xml) - Extensible Markup Language files

## File Upload Constraints:

- **Maximum number of files**: 5 files per upload
- **Maximum file size**: 100 MB per file
- All files are indexed and processed for efficient search and retrieval

## Managing Existing File Sources:

- Switch to the **Existing File** tab to view and manage previously created file sources
- The system displays the total number of available sources at the top-right corner
- You can edit, delete, or update permissions for existing file sources as needed

## Resource Optimization Recommendations for Batch File Processing

The following table outlines the estimated data indexing capacity for various Kubernetes pod tiers. 
Each estimate assumes files of approximately 10 MB each and accounts for typical memory and I/O requirements during chunking, embedding, and batching operations. 

This guide helps determine the appropriate pod size for different dataset volumes, ensuring smooth operation without excessive swapping or slowdowns. 


| **Tier**   | **vCPUs**      | **RAM**   | **Max Files (10 MB each)** | **Total Data Volume** |
|-------------|----------------|-----------|-----------------------------|------------------------|
| Small       | 1 core         | 2 GB      | ~500 files                  | ~5 GB                 |
| Medium      | 2 cores        | 4 GB      | ~2,000 files                | ~20 GB                |
| Large       | 4 cores        | 8 GB      | ~5,000 files                | ~50 GB                |
| X-Large     | 4–6 cores      | 16 GB     | ~10,000 files               | ~100 GB               |
| XX-Large    | 8 cores        | 32 GB     | 15,000+ files               | ~150–200 GB           |

**Note**: These estimates are based on an average file size of 10 MB each. Actual performance and capacity may vary depending on several factors such as file size variability, number of pages, content density, and processing overhead. 