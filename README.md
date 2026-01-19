# GTM Demo (Technical Assessment)

**Live site:** [https://simonderstine.github.io/gtm-demo/](https://simonderstine.github.io/gtm-demo/)

## Overview
This project demonstrates:
1. Google Tag Manager (GTM) implementation on a simple GitHub Pages site
2. Capturing URL query parameters and pushing them into the GTM dataLayer
3. Clicking a button to send a GET request to `https://httpbin.org/get` using values stored from the query string
4. Logging the API response in the browser console

## Technologies Used
- Google Tag Manager (GTM)
- GitHub Pages
- JavaScript (Fetch API)
- httpbin.org (test API)

## How to Test

### 1. Load the page with query parameters
https://simonderstine.github.io/gtm-demo/?key=key&value=value

### 2. Verify dataLayer capture
  - Go to tagmanager.google.com → Preview
  - Connect to your live URL
  - Refresh the page → look for the `querystring_captured` event

### 3. Click the button to send the API request
- Click **Send API Request**
- Open DevTools → Console tab
- The response should contain:
    - `args: { key: "key", value: "value" }`
    - `url: "https://httpbin.org/get?key=key&value=value"`

