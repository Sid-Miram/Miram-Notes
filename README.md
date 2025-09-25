# Miram-Notes

Absolutely! Here’s a detailed **README** template for your YouTube Notes Taker & Video Summarizer Chrome Extension, designed for Manifest v3, including both the API key input and OAuth options.

Feel free to customize it as you build!

---

# EduTube AI — YouTube Notes Taker & Video Summarizer Chrome Extension

![EduTube AI Logo](https://your-logo-url-here.png)

---

## Overview

**EduTube AI** is a free, privacy-focused Chrome extension that enhances your learning experience on YouTube by:

* Automatically detecting educational videos
* Providing a floating sidebar to take **timestamped notes**
* Generating AI-powered **video summaries**
* Allowing you to **ask questions** about the video content
* Supporting **two API key management options**:

  * **User-supplied API key** (for technical users)
  * **OAuth integration** to manage API keys on behalf of non-technical users

All data is stored locally — no backend server required (unless you use OAuth, which requires a minimal backend to handle authentication).

---

## Features

* Detects educational videos by analyzing video title and description
* Floating sidebar for notes, summaries, and Q&A
* Timestamped notes synced to video playback time
* Summarizes video transcripts using AI APIs (OpenAI, Gemini, Claude, etc.)
* Ask AI questions about the video content for deeper understanding
* Supports local storage of notes and API keys
* OAuth option to simplify API key management for non-technical users
* Manifest v3 compatible for Chrome’s latest extension standards

---

## Getting Started

### Installation

1. Download or clone this repository
2. Open Chrome and go to `chrome://extensions/`
3. Enable **Developer Mode** (top right)
4. Click **Load unpacked** and select the project folder
5. The EduTube AI extension icon should appear next to the address bar

---

### Configuration

Upon first use, configure your API access:

* **Option 1: Enter your own API key**

  * Go to the extension’s popup or settings sidebar
  * Paste your OpenAI/Gemini/Claude API key
  * The key is stored locally and used for AI calls

* **Option 2: Use OAuth** (requires backend setup)

  * Click "Sign in with OAuth"
  * Follow the authentication process
  * The backend manages API keys securely for you

---

## Usage

1. Open a YouTube video categorized as educational or manually activate the sidebar
2. Use the sidebar to:

   * Take notes (auto-timestamped to current video time)
   * View AI-generated summaries of the video transcript
   * Ask questions and receive AI answers in real-time
3. Export your notes anytime as Markdown or plain text

---

## Architecture

| Component       | Description                                     |
| --------------- | ----------------------------------------------- |
| `manifest.json` | Extension manifest file (Manifest v3)           |
| `content.js`    | Injects sidebar UI and detects video state      |
| `sidebar.html`  | Sidebar UI markup                               |
| `sidebar.js`    | Handles UI logic, note taking, AI API calls     |
| `background.js` | Service worker for OAuth and background tasks   |
| `api/`          | Modules for interacting with different AI APIs  |
| `utils/`        | Helper functions (transcript fetching, storage) |

---

## Permissions

* `storage` — to save notes and API keys locally
* `activeTab` — to detect YouTube video content
* `identity` — (optional) for OAuth authentication
* `scripting` — to inject content scripts and UI

---

## Development

### Building and Testing

* Use Chrome’s developer mode to load the unpacked extension
* Modify UI and scripts as needed
* Use console logs for debugging content scripts and service worker

---

## Contributing

Contributions and suggestions are welcome! Feel free to open issues or submit pull requests.

---

## License

MIT License © 2025 Your Name

---

## FAQ

**Q:** Do I need an OpenAI API key?
**A:** Yes, unless you use the OAuth option. You must provide a valid API key for AI features.

**Q:** Is my data sent to any server?
**A:** No, all data is stored locally in your browser. OAuth may send minimal data to your backend for authentication.

**Q:** Does it work on Firefox or other browsers?
**A:** Currently designed for Chrome with Manifest v3, but could be adapted.

---

If you want, I can help generate:

* A sample `manifest.json`
* Basic folder structure
* Starter code snippets for API key input and sidebar UI

Just ask!
