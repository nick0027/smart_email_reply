# Email Reply Generator

## Overview
The **Email Reply Generator** is a web application that helps users generate AI-powered email responses. It takes an input email, allows users to select a tone (e.g., professional, casual, friendly), and generates a response using an AI-based backend. The project consists of a **React frontend** and a **Spring Boot backend**, communicating via a REST API.

## Features
- Input email content
- Select a tone for the reply
- Generate AI-powered responses
- Copy generated reply to clipboard
- Handles loading and error states gracefully

## Technologies Used
### Frontend (React with Material UI)
- React.js with Vite
- Material UI for UI components
- Axios for API requests
- React hooks (`useState`) for state management

### Backend (Spring Boot with WebClient)
- Spring Boot
- REST API using `@RestController`
- WebClient for API communication
- JSON processing with Jackson
- Lombok for reducing boilerplate code

## Installation & Setup
### Backend
1. Clone the repository:
   ```sh
   git clone https://github.com/yourusername/email-reply-generator.git
   cd email-reply-generator/backend
   ```
2. Configure API key for AI service:
   - Update `application.properties` with `gemini.api.url` and `gemini.api.key`.
3. Run the Spring Boot application:
   ```sh
   mvn spring-boot:run
   ```

### Frontend
1. Navigate to the frontend folder:
   ```sh
   cd ../frontend
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the development server:
   ```sh
   npm run dev
   ```
4. Open the app in your browser at:
   ```
   http://localhost:5173
   ```

## API Endpoint
- **POST /api/email/generate**
  - Request Body:
    ```json
    {
      "emailContent": "Your email content here",
      "tone": "professional"
    }
    ```
  - Response:
    ```json
    {
      "generatedReply": "AI-generated email reply."
    }
    ```

## Usage
1. Enter the original email content.
2. Select the desired tone (optional).
3. Click **Generate Reply**.
4. Copy the generated response and use it in your email.

## Future Improvements
- Add more tone options
- Integrate authentication
- Improve AI response customization

## License
This project is open-source under the MIT License.

