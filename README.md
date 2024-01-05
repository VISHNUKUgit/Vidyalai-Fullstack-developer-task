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
   git clone https://github.com/VISHNUKUgit/Vidyalai-Fullstack-developer-task.git
   cd Split-PDF
   
   cd split-pdf
   npm i sweetalert2
   npm i react-router-dom
   npm i react-pdf
   npm install react-bootstrap bootstrap
   npm install axios
   npm install @mui/material @emotion/react @emotion/styled
   npm i file-saver

   cd ../split-pdf-server
   npm i cors
   npm i dotenv
   npm i express
   npm i mongoose
   npm i multer
   npm i pdf-lib
   
2. Start the frontend
   ```bash
   cd split-pdf
   npm start

4. Start the backend
   ```bash
   cd ../split-pdf-server
   node index.js

## Usage

1. Open the web application in your browser.
2. To access the application, start by navigating through the authentication process
3. Upload a PDF file using the provided form; this action will automatically populate the list with all available PDFs.
4. Choose the specific PDF file you want to modify from the list of available PDFs
5. Select the pages you wish to extract from the selected PDF.
6. Click the 'Generate New PDF' button to create a new PDF.
7. Download the newly created PDF by clicking the "Download PDF" button.
8. If you prefer to rearrange pages before downloading, select "Rearrange Pages & Download"

## API Documentation

### POST /user/register
- Description: Register a user account.
- Request body: Include user data (username, email, password).
- Response: 
      -successful : Return a status 200 (OK) and the newly created user details.
      -error      : return a status 401 (Unauthorized) with the error message
                  : If a user with the email already exists, return a status 406 (Not Acceptable)
### POST /user/login
- Description: Authenticate a user.
- Request body: Include user data (email, password).
- Response: 
      -successful : Return a status 200 (OK) with the user details
      -error      : If no matching user is found, return a status 404 (Not Found) with an error message
                  : If an error occurs during the login process, return a status 401 (Unauthorized) with the error message

### POST /upload
- Description: Extract selected pages and create a new PDF.
- Request body:  Include uploderId:_id,title for the file,files:filename.
- Response: 
      -successful : Return a status 200 (OK) with the added file information
      -error      : return a status 401 (Unauthorized) with the error message

### POST /get_pdf
- Description: Retrieve a stored PDF.
- Request body:  Include uploderId:userId .
- Response: 
      -successful : Return a status 200 (OK) with the list of files
      -error      : return a status 401 (Unauthorized) with the error message

### POST /create-new-pdf
- Description: Extract selected pages and create a new PDF.
- Request body: Include fileName:files && pageNumber.
- Response: 
      -successful : Return a status 200 (OK) wuth the modified file name as a response
      -error      :  Return a status 500 (Internal Server Error) with the error message

### POST /rearrange-download-pdf
- Description: create a new PDF with rearranged pages  .
- Request body: fileName:modified file name && pageNumber.
- Response: 
      -successful : Return a status 200 (OK) wuth the modified file name as a response
      -error      : Return a status 500 (Internal Server Error) with the error message
  
