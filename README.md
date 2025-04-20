# CorrectMe Web

A web application for AI-powered text correction and translation.

## Features

*   **Text Correction:** Get your text corrected by an AI, complete with explanations for the changes and a visual diff highlighting the modifications.
*   **Text Translation:** Translate text into various target languages.
*   **Language Detection:** Automatically detects the language of the input text for more accurate corrections.
*   **Internationalized UI:** The user interface is available in English and Portuguese (Brazil).
*   **Theme Toggle:** Switch between Light and Dark themes for comfortable viewing.
*   **Local API Key Storage:** Securely store your LLM API key locally in your browser via the Settings modal.
*   **Streaming Responses:** Corrections are streamed back for a more responsive experience.

## How it Works

CorrectMe Web provides a simple interface for text manipulation:

1.  Enter your text into the appropriate text area (Correction or Translation tab).
2.  For corrections, click the "Correct" button. The app detects the language, sends the text to the configured LLM API (via OpenRouter.ai by default), streams the corrected text and explanations back, and displays a visual difference using `htmldiff.js`.
3.  For translations, select the target language and click "Translate". The app sends the text and target language to the LLM API and displays the translation.
4.  A settings modal allows you to enter and save your API key, which is necessary for the AI features to function. This key is stored only in your browser's `localStorage`.

## Technology Stack

*   HTML5
*   CSS3
*   Vanilla JavaScript (ES6+)
*   [htmldiff.js](https://github.com/tnwinc/htmldiff.js) (included locally) - For visualizing text differences.
*   [OpenRouter.ai API](https://openrouter.ai/) (or potentially other LLM providers) - For the AI correction and translation capabilities.

## Setup & Usage

1.  Clone this repository or download the files.
2.  Open the `index.html` file directly in your web browser.
3.  **Important:** Click the "Settings" button and enter your API key (e.g., from OpenRouter.ai). The correction and translation features will not work without a valid API key. The key is saved locally in your browser's storage for future sessions.
4.  Start correcting or translating text!

## Localization

The user interface supports multiple languages. Translation files are located in the `locales/` directory:

*   `locales/en.json`: English
*   `locales/pt-BR.json`: Portuguese (Brazil)

The application detects the browser's preferred language or uses the language selected via the UI buttons/localStorage.
