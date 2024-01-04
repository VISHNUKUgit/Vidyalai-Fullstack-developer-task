# Vidyalai-Fullstack-developer-task
A web application that allows users to upload a PDF file, extract selected pages, and download a new PDF.
## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [API Documentation](#api-documentation)
- 
## Features
- User authentication
- File upload for PDFs
- View upoaded PDFs
- Visual representation of PDF pages
- Page selection for extraction
- Rearrange the order of selected pages
- Download of newly created PDF
- 
## Technologies Used

- React.js for the frontend
- Node.js with Express for the backend
- React-PDF for displaing PDF pages
- pdf-lib for PDF manipulation
- Multer for uploading files
- 
## Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/pdf-extractor.git
   cd pdf-extractor
   
2. To run Frontend :
  ```bash
cd frontend
npm start

3. To run Backend :
  ```bash
      cd ../backend
      npm index.js

# For the backend, create a .env file with necessary variables
# Start the frontend
cd frontend
npm start

# Start the backend
cd ../backend
npm start
6. **Usage:**
   - Explain how users can interact with your application.

```markdown
## Usage

1. Open the web application in your browser.
2. Upload a PDF file using the provided form.
3. Visualize the PDF pages and select the ones you want to extract.
4. Click the 'Extract' button to create a new PDF.
5. Download the newly created PDF.
## API Documentation

### POST /api/upload
- Description: Upload a PDF file.
- Request body: FormData with PDF file.
- Response: Status 200 if successful.

### GET /api/pdf/:id
- Description: Retrieve a stored PDF.
- Parameters: PDF ID.
- Response: PDF file.

### POST /api/extract
- Description: Extract selected pages and create a new PDF.
- Request body: JSON with selected page numbers.
- Response: Newly created PDF file.
  
