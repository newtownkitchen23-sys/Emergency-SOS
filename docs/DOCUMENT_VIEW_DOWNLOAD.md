# Document View and Download Endpoints

## API Endpoints

### 1. View Document
- **Endpoint:** `/api/documents/view/{documentId}`  
- **Method:** `GET`  
- **Description:** Retrieves the metadata and viewable content of the specified document.  
- **Parameters:**  
  - `documentId` (required): The unique identifier of the document to be viewed.  
- **Response:**  
  - `200 OK`: Successful retrieval of document data.  
  - `404 Not Found`: Document not found.  

### 2. Download Document
- **Endpoint:** `/api/documents/download/{documentId}`  
- **Method:** `GET`  
- **Description:** Allows users to download the specified document.  
- **Parameters:**  
  - `documentId` (required): The unique identifier of the document to be downloaded.  
- **Response:**  
  - `200 OK`: Document successfully downloaded.  
  - `404 Not Found`: Document not found.  
  - `403 Forbidden`: User does not have permission to download this document.

## Usage Examples

### View Document Example  
```bash  
curl -X GET http://yourdomain.com/api/documents/view/123456
```

### Download Document Example  
```bash  
curl -X GET http://yourdomain.com/api/documents/download/123456
```

## Error Handling
- Ensure to validate `documentId` parameter.
- Handle possible exceptions or errors gracefully in your application.