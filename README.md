# Project Title

**Frontend Repository:** [https://github.com/tayyipcanbay/PromptPro-Frontend]

**Backend Repository:** [https://github.com/tayyipcanbay/PromptPro-Backend]

## Table of Contents

- [Project Overview](#project-overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Frontend Setup](#frontend-setup)
- [Backend Setup](#backend-setup)
- [Usage](#usage)
- [API Endpoints](#api-endpoints)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Project Overview

This project is a comprehensive web application that allows users to interact with an intelligent chatbot through both text and image inputs. It includes a frontend built with React and a backend powered by Flask. The application leverages Tesseract OCR for image processing and OpenAI's GPT-3.5 model for generating responses. Users can authenticate using their email and token, and then engage with the chatbot to get assistance or information. 

Check out the project demonstration in the video below:

[![Project Video](https://youtu.be/vQKSom6TVeE.jpg)](https://youtu.be/vQKSom6TVeE)


## Features

- User authentication and authorization
- Text-based chat with the chatbot
- Image upload and processing with Tesseract OCR
- Responses generated using OpenAI's GPT-3.5 model
- Drag-and-drop file upload functionality

## Technologies Used

### Frontend:
- React
- React Router
- Axios
- CSS for styling

### Backend:
- Flask
- Flask-CORS
- OpenAI API
- Tesseract OCR
- SQLite (for user management)

## Frontend Setup

### Prerequisites

- Node.js
- npm

### Installation

1. Clone the repository:

    ```bash
    git clone [https://github.com/tayyipcanbay/PromptPro-Frontend]
    cd PromptPro-Frontend
    ```

2. Install dependencies:

    ```bash
    npm install
    ```

3. Start the development server:

    ```bash
    npm start
    ```

The application will be available at `http://localhost:3000`.

### File Structure
src/
|– pages/
|   |– Ask.js
|   |– LoginPage.js
|   |– WelcomePage.js
|– App.js
|– index.js
|– App.css
|– index.css

## Backend Setup

### Prerequisites

- Python 3.7+
- pip

### Installation

1. Clone the repository:

    ```bash
    git clone [https://github.com/tayyipcanbay/PromptPro-Backend]
    cd PromptPro-Backend
    ```

2. Create a virtual environment and activate it:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

4. Set up environment variables:

    Create a `.env` file in the root directory and add your OpenAI API key:

    ```
    OPENAI_API_KEY=your_openai_api_key
    ```

5. Start the server:

    ```bash
    python flask_app.py
    ```

The backend server will be available at `http://localhost:5500`.

### File Structure

backend-repo/
|– flask_app.py
|– gpt_request.py
|– tesseract_operations.py
|– database_operations.py
|– requirements.txt

## Usage

1. Open the frontend application in your browser (`http://localhost:3000`).
2. Navigate to the login page and enter your email and token.
3. Once logged in, you can interact with the chatbot by sending text messages or uploading images.

## API Endpoints

### `POST /login`
- Authenticates a user and returns a user ID.
- Request Body: `{ "email": "user@example.com", "token": "user_token" }`

### `POST /ask-text`
- Sends a text query to the chatbot and returns the response.
- Request Body: `{ "text": "your question", "email": "user@example.com", "token": "user_token" }`

### `POST /ask-image`
- Uploads an image, extracts text using Tesseract OCR, and sends the text to the chatbot.
- Request Body: Form data containing the image file, email, token, and additional text.

## Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make your changes.
4. Commit your changes (`git commit -m 'Add some feature'`).
5. Push to the branch (`git push origin feature-branch`).
6. Open a pull request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or suggestions, feel free to contact me at `tayyipcanbaydev@gmail.com`.
