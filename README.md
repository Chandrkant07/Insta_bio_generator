# ✨ AI Instagram Bio Generator ✨

A simple, single-file web application that uses AI (via OpenRouter) to generate creative and personalized Instagram bio suggestions based on user inputs.

## Description

This tool helps users craft engaging Instagram bios by providing AI-powered suggestions. Users input their name, profession, and interests, select a desired tone, and choose whether to include emojis. The application then queries an AI model through the OpenRouter API and displays several bio options tailored to the user's input. It also includes a basic ad integration.

**Note:** This project is provided as a single `index.html` file containing HTML, CSS, and JavaScript for demonstration purposes.

## Features

*   **User Inputs:** Accepts Name, Profession, and comma-separated Interests.
*   **Tone Selection:** Allows users to choose a desired tone (e.g., Professional, Cool, Funny, Aesthetic) via interactive buttons.
*   **Emoji Option:** Toggle to include or exclude emojis in the generated bios.
*   **AI-Powered Suggestions:** Connects to the OpenRouter API to leverage AI models (like Mistral or Deepseek) for bio generation.
*   **Multiple Outputs:** Displays up to 3 unique bio suggestions.
*   **Copy Functionality:** Provides a "Copy" button for each suggestion.
*   **Responsive Design:** Basic responsiveness for different screen sizes.
*   **Ad Integration:** Includes a placeholder and scripts for a 468x60 ad banner from `highperformanceformat.com`.
*   **Single-File Structure:** All code (HTML, CSS, JS) is contained within one `index.html` file for simplicity.

## Screenshot

![image](https://github.com/user-attachments/assets/7d184e1d-1edd-4607-beba-f8d4a126960e)


## Prerequisites

*   A modern web browser (Chrome, Firefox, Edge, Safari recommended).
*   An active **OpenRouter API Key**. Get one from [OpenRouter.ai](https://openrouter.ai/).
*   Internet connection (for API calls and loading ads).

## Setup and Installation

1.  **Save the Code:** Save the complete HTML code provided in the previous step as `index.html`.
2.  **Add API Key:**
    *   Open the `index.html` file in a text editor.
    *   Locate the `<script>` block near the end of the file containing the main application logic.
    *   Find the line:
        ```javascript
        const API_KEY = 'sk-or-v1-b6ec0...'; // Replace with your actual key
        ```
    *   **CRITICAL:** Replace the placeholder `'sk-or-v1-...'` with your **actual OpenRouter API Key**.
    *   **⚠️ SECURITY WARNING:** Never commit your actual API key to version control (like Git) or deploy this file publicly with the key embedded directly in the client-side JavaScript. For production use, implement a backend proxy server to handle API requests securely.
3.  **Run on a Web Server:**
    *   **Do NOT simply double-click and open the `index.html` file directly in your browser using the `file:///` protocol.** API calls and external ad scripts often fail due to security restrictions when run this way.
    *   You **MUST** serve the `index.html` file using a local web server. Options include:
        *   Using the VS Code "Live Server" extension.
        *   Python's built-in server: Navigate to the file's directory in your terminal and run `python -m http.server` (or `python3 -m http.server`) and then access `http://localhost:8000` in your browser.
        *   Node.js `http-server`: Install via `npm install -g http-server`, navigate to the directory, run `http-server`, and access the provided local address.
4.  **Disable Ad Blocker (for Ad Testing):** If you want to test if the ad banner is loading correctly, you **MUST** disable any ad-blocking browser extensions (like AdBlock, uBlock Origin) for the local server address (e.g., `localhost` or `127.0.0.1`).

## Usage

1.  Access the `index.html` file through your local web server's address in your browser.
2.  Enter your Name, Profession, and Interests in the respective input fields.
3.  Click on the button corresponding to the desired Tone (e.g., "Funny", "Professional"). The active tone will be highlighted.
4.  Check or uncheck the "Include Emojis" box as desired.
5.  Click the "Generate Bios" button.
6.  Wait a few moments while the AI generates suggestions. The button will show a "Generating..." state.
7.  View the generated bio suggestions in the "Your Bio Suggestions" section.
8.  Click the "Copy" button next to any suggestion to copy it to your clipboard.

## Technology Stack

*   **Frontend:** HTML5, CSS3, JavaScript (ES6+)
*   **AI API:** [OpenRouter.ai](https://openrouter.ai/) (using models like Mistral or Deepseek)
*   **Advertising:** Ad script integration via `highperformanceformat.com`

## Important Considerations & Warnings

*   **API Key Security:** **EXTREMELY IMPORTANT!** The current setup embeds your OpenRouter API key directly in the client-side JavaScript. This is **highly insecure** and makes your key visible to anyone inspecting the page source. **NEVER** deploy this code publicly with your real key embedded. Use a backend proxy for any production or shared environment.
*   **Ad Loading:** Ads may not display if:
    *   An ad blocker is active.
    *   You are running the file directly using `file:///`.
    *   The ad network has low fill rates for your region/context.
    *   Your domain/localhost is not approved by the ad network.
*   **AI Output:** AI-generated content can sometimes be unpredictable or require editing. Always review the suggestions before using them on your actual Instagram profile.
*   **Rate Limits & Costs:** Be mindful of potential API usage limits and costs associated with your OpenRouter account, even for "free" models which often have usage caps.

## Contributing

This is a basic example project. Contributions or suggestions for improvement are welcome (if applicable, e.g., if hosted on GitHub). Please follow standard coding practices.

## License

*(Optional: Add a license if you plan to share this code, e.g., MIT License)*

