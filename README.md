# Concept Explainer

A simple web application that explains complex concepts in simple words using local Large Language Models (LLMs).

## Overview

Concept Explainer is a lightweight web application that uses locally running LLMs (via Ollama) to provide clear explanations for complex topics without sending any data to external APIs. The application features a clean, responsive interface that allows users to:

- Enter any concept or topic they want explained
- Adjust the temperature (creativity) of the response
- Choose from multiple local LLM models (Llama 3, Mistral, Gemma)
- Receive instant explanations generated entirely on their local machine

## Prerequisites

- [Node.js](https://nodejs.org/) (v14 or higher)
- [Ollama](https://ollama.ai/) - An application for running LLMs locally
- One or more models pulled to your Ollama installation:
  - llama3
  - mistral
  - gemma

## Installation

1. Clone this repository:
   ```
   git clone <repository-url>
   cd concept-explainer
   ```

2. Install dependencies:
   ```
   npm install
   ```

3. Create a `.env` file:
   ```
   cp .env-example .env
   ```

4. Make sure Ollama is running with the required models:
   ```
   ollama pull llama3
   ollama pull mistral
   ollama pull gemma
   ollama run llama3
   ```

## Usage

1. Start the application:
   ```
   npm start
   ```

2. Open your browser and navigate to:
   ```
   http://localhost:3000
   ```

3. Enter a concept or topic in the text area, adjust the temperature slider if desired, select a model, and click "Explain".

4. The explanation will appear in the output section.

## Development

To start the application in development mode with auto-restart on file changes:

```
npm run dev
```

## Features

- **Privacy-Focused**: All processing happens locally - no data is sent to external APIs
- **Responsive Design**: Works on desktop and mobile devices
- **Adjustable Parameters**: Control the temperature (creativity) of the response
- **Multiple Models**: Choose between different LLM models based on your needs
- **Request Logging**: All requests and responses are logged for future reference

## Troubleshooting

- If you see a warning banner saying "Could not connect to Ollama", make sure Ollama is running on your machine
- Check the `logs/explanations.log` file for detailed request and response logs

## Project Structure

- `server.js` - Express server and API endpoints
- `public/` - Frontend files
  - `index.html` - Main HTML file
  - `script.js` - Frontend JavaScript
  - `style.css` - CSS styles
- `logs/` - Request and response logs (created automatically)

## License

MIT