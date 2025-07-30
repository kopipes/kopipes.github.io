# Deploying Your Translator App

This directory contains the built, production-ready version of your Real-time Conversation Translator. You can deploy the contents of this folder to any static web hosting service (like Vercel, Netlify, GitHub Pages, etc.).

## ❗️ Important: Setting Your API Key

For the Gemini translation service to work, you must provide your API key. In a deployed application, you cannot use `process.env` the same way you do in a local development environment.

### How to Add Your API Key

1.  **Open `index.html`:** Open the `index.html` file in a text editor.

2.  **Find the API Key Placeholder:** Near the top of the large `<script type="module">` block at the bottom of the file, find this line:

    ```javascript
    const API_KEY = process.env.API_KEY || null;
    ```

3.  **Replace with Your Key:** Replace `process.env.API_KEY || null` with your actual Gemini API key in quotes.

    **Before:**
    ```javascript
    const API_KEY = process.env.API_KEY || null;
    ```

    **After:**
    ```javascript
    const API_KEY = "YOUR_GEMINI_API_KEY_HERE"; 
    ```

4.  **Save and Deploy:** Save the `index.html` file. Now you can upload this modified file (along with this README) to your hosting service.

Your application should now be fully functional online.
