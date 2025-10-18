🤖 AI-Powered Code Reviewer (NER Stack + Gemini API)
Vercel :https://code-review-yx3v.vercel.app/
🌟 Project Overview

This is an NER (Node.js, Express, React) stack application designed to help developers quickly identify and fix errors in their code. It integrates the Google Gemini API to analyze submitted code and provide detailed, intelligent reviews, explanations, and suggested fixes for any issues found.

The project features a clear, two-panel interface: one for code input and one for the AI-generated review, ensuring a smooth and readable user experience.

✨ Key Features

Intelligent Code Analysis: Uses the Gemini 2.5 Flash model (or similar) via the official SDK to check code snippets for errors, best practices, and suggestions.

NER Stack Architecture: Built on a robust and scalable architecture with a dedicated React frontend and Node.js/Express backend.

Modular API Design: A dedicated backend route (/ai/get-review) handles code submission and secure interaction with the Gemini SDK.

Readable Output: The output panel is styled with a white background and dark text for optimal readability, overriding the application's overall dark theme.

🛠️ Tech Stack

Component

Technology

Role

Frontend

React

User Interface and Input Handling

Backend

Node.js, Express.js

API Handling and Server Logic

AI Integration

@google/generative-ai

Communicates with the Gemini API

Utility

dotenv, cors, nodemon

Environment variables, CORS handling, and dev server monitoring

🚀 Getting Started

Prerequisites

Node.js (v18+) and npm

A Gemini API Key (required for the backend)

Installation

Follow these steps to set up the backend and frontend locally.

Clone the repository:

git clone [YOUR_REPO_URL]


Backend Setup (Navigate to the API folder, confirmed by package.json)

cd code-review-main/BackEnd
npm install


Create a file named .env in the BackEnd directory and add your API key and port configuration:

# .env in the BackEnd folder
GEMINI_API_KEY="YOUR_GEMINI_API_KEY_HERE"
PORT=8080 


Frontend Setup (Navigate to the React folder)

cd ../FrontEnd 
npm install


⚙️ Running the Application

You must run the backend and frontend in two separate terminal windows.

1. Start the Backend API

From the BackEnd directory:

cd code-review-main/BackEnd
npx nodemon 
# Server should start and listen on port 8080


2. Start the Frontend App

From the FrontEnd directory:

cd ../FrontEnd
npm run dev 
# The app will open in your browser (e.g., http://localhost:5173)


💻 Usage

Open the application in your browser.

Paste the code you want reviewed into the left-hand input box.

The frontend sends a POST request to the backend endpoint: http://localhost:8080/ai/get-review.

The backend processes the request via the Gemini API.

The detailed AI review is displayed on the right-hand output panel.

 