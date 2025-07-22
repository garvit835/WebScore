# WebScore - Website Legitimacy Checker

![WebScore](https://placehold.co/800x400/111827/ffffff?text=WebScore%20Screenshot)

<p align="center">
  <img alt="License" src="https://img.shields.io/badge/License-Apache_2.0-blue.svg"/>
  <img alt="Open Source" src="https://img.shields.io/badge/Open%20Source-❤️-brightgreen"/>
</p>

A simple, client-side tool that performs basic OSINT (Open-Source Intelligence) checks on a given URL to help users assess its legitimacy and potential risk.

**🔗 Live Demo: [https://garvit835.github.io/WebScore/](https://garvit835.github.io/WebScore/)**

---

## 🤔 The Problem: Is This Site Legit?

We've all hesitated before clicking a link, wondering, "Is this website legit or a scam?" Scammers are becoming increasingly sophisticated, making it difficult to distinguish safe websites from malicious ones. This tool was created to provide a quick, first-glance analysis to help users make a more informed decision.

## ✨ Core Features

WebScore generates a "Trust Score" based on a combination of the following checks:

* **🔍 Google Safe Browsing:** Checks the URL against Google's massive, constantly updated blacklist of malicious websites (phishing, malware, etc.).
* **📅 Domain Age:** Looks up the domain's creation date. Very new domains are often a red flag for scam sites.
* **📜 Web Archive History:** Checks the Internet Archive's Wayback Machine to see if the website has a long-standing digital footprint.
* **🔒 HTTPS Usage:** A basic check to see if the site uses a secure connection.

## 🚀 Under the Hood: How It Works

This project is built entirely with **HTML, CSS, and client-side JavaScript**, meaning it runs completely in your browser. There is no backend server. It leverages free, third-party APIs to gather data:

1.  The user enters a URL.
2.  JavaScript makes simultaneous `fetch` requests to various APIs.
3.  The responses are collected and analyzed by a simple scoring algorithm.
4.  A final report card is generated and displayed to the user.

## 🛠️ Get It Running Locally

To run this project locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/garvit835/WebScore.git](https://github.com/garvit835/WebScore.git)
    ```

2.  **Get API Keys:** This tool requires two free API keys to function.

    * **Google Safe Browsing API:**
        * Go to the [Google Cloud Console](https://console.cloud.google.com/).
        * Create a new project.
        * Enable the "Safe Browsing API".
        * Go to "Credentials" and create a new "API key".

    * **WhoisXML API:**
        * Create a free account at [WhoisXMLAPI.com](https://www.whoisxmlapi.com/).
        * Your API key will be available on your account dashboard.

3.  **Add Keys to the Code:**
    * Open the `index.html` file.
    * Find the `<script>` section at the bottom.
    * Paste your keys into the `GOOGLE_SAFE_BROWSING_API_KEY` and `WHOIS_API_KEY` constants.

    ```javascript
    const GOOGLE_SAFE_BROWSING_API_KEY = 'YOUR_GOOGLE_KEY_HERE';
    const WHOIS_API_KEY = 'YOUR_WHOISXMLAPI_KEY_HERE';
    ```

4.  **Open in Browser:**
    * Simply open the `index.html` file in your web browser.

## 💻 Tech Stack

<p align="left">
  <img alt="HTML5" src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white"/>
  <img alt="TailwindCSS" src="https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white"/>
  <img alt="JavaScript" src="https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black"/>
</p>

* **HTML5**
* **Tailwind CSS** for styling.
* **Vanilla JavaScript** for all logic and API calls.

---

## ⚠️ Important Disclaimer

This tool is intended for educational purposes and as a preliminary check. It is **not a guarantee** of a website's safety. Always use your own judgment and be cautious when browsing unfamiliar websites.

## 📄 License

This project is licensed under the Apache License 2.0. See the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgements

This tool would not be possible without the free and accessible APIs provided by:

* [Google Safe Browsing](https://developers.google.com/safe-browsing)
* [WhoisXML API](https://www.whoisxmlapi.com/)
* [Internet Archive Wayback Machine](https://archive.org/help/wayback_api.php)
