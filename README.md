# AI Performance Coach

AI Performance Coach is an AI-powered web application designed to help users improve their productivity, performance, and daily work habits. The application uses AI models to analyze user inputs and provide personalized insights, suggestions, and performance guidance.

## Project Overview

The AI Performance Coach allows users to interact with an AI-powered coaching system through a web interface.

The application can:

* Provide AI-powered performance coaching
* Analyze user information and performance
* Generate personalized recommendations
* Use different AI providers depending on the configured API keys
* Support multiple AI/LLM providers
* Provide a web-based user interface
* Run locally using a Python backend

The project is designed with a flexible architecture so that different AI providers can be configured through environment variables.

## Technologies Used

### Frontend

* HTML5
* CSS3
* JavaScript

### Backend

* Python
* REST APIs
* HTTP server

### AI / LLM Providers

The application can be configured to use supported AI providers such as:

* Google Gemini
* OpenAI
* Anthropic Claude
* Groq
* xAI
* OpenRouter
* NVIDIA NIM
* Ollama

The available providers depend on the configuration implemented in the project.

### Deployment

* Vercel
* Python serverless functions

## Setup and Installation

### 1. Download or Clone the Project

Download the project and open the project folder in VS Code or another code editor.

### 2. Open the Project Directory

```bash
cd ai-performance-coach
```

### 3. Create a Python Virtual Environment

On Windows:

```powershell
python -m venv venv
```

Activate the virtual environment:

```powershell
venv\Scripts\activate
```

### 4. Install Dependencies

If the project contains a `requirements.txt` file:

```powershell
pip install -r requirements.txt
```

## API Key Configuration

Create a `.env` file in the project root directory.

Example:

```env
GEMINI_API_KEY=your_gemini_api_key
OPENAI_API_KEY=your_openai_api_key
ANTHROPIC_API_KEY=your_anthropic_api_key
GROQ_API_KEY=your_groq_api_key
XAI_API_KEY=your_xai_api_key
OPENROUTER_API_KEY=your_openrouter_api_key
NVIDIA_API_KEY=your_nvidia_api_key
OLLAMA_API_KEY=your_ollama_api_key
```

Only add the API keys for the providers you want to use.

For example:

```env
GEMINI_API_KEY=your_key_here
GROQ_API_KEY=your_key_here
NVIDIA_API_KEY=your_key_here
```

Do not upload your actual API keys to GitHub.

Make sure `.env` is included in `.gitignore`.

## How to Run the Project

After activating the virtual environment and configuring your API keys, run the backend from the project root directory:

```powershell
python lib/backend.py
```

If the server starts successfully, it will display the local address in the terminal.

Open that address in your browser.

For example:

```text
http://localhost:5000
```

The exact port depends on the backend configuration.

## Project Structure

```text
ai-performance-coach/
│
├── api/
│   └── ...
│
├── lib/
│   └── backend.py
│
├── index.html
├── .env.example
├── .gitignore
├── README.md
└── ...
```

### Important Files

**`index.html`**

Contains the frontend interface of the application.

**`lib/backend.py`**

Contains the Python backend and API/server functionality.

**`.env.example`**

Provides an example of the environment variables required by the application.

**`.env`**

Contains private API keys and configuration. This file should not be committed to GitHub.

## Deployment

The project also contains API/serverless components that can be deployed using Vercel.

Before deploying:

1. Push the project to GitHub.
2. Import the repository into Vercel.
3. Configure the required environment variables in Vercel.
4. Add your API keys under Environment Variables.
5. Deploy the project.

Do not put API keys directly inside frontend HTML or JavaScript files.

## Security

API keys should always be stored as environment variables.

Never write API keys directly in:

```text
index.html
JavaScript files
Python source code
GitHub repositories
```

Instead, use environment variables:

```env
API_KEY=your_key_here
```

## Quick Start

```powershell
cd ai-performance-coach
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python lib/backend.py
```

Then open the local URL displayed in the terminal.

## Notes

* Make sure Python is installed and available from the command line.
* Make sure all required dependencies are installed.
* Configure at least one supported AI provider before using the AI features.
* Keep your API keys private.
* If an API provider is unavailable, configure another supported provider when fallback support is available.

## License

This project is intended for educational and development purposes.
