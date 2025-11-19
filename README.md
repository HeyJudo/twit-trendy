<div align="center">

# 🐦 Twitter Trends Visualizer

**A dynamic data visualization dashboard tracking real-time Twitter/X trends.**

![JavaScript](https://img.shields.io/badge/javascript-%23323330.svg?style=for-the-badge&logo=javascript&logoColor=%23F7DF1E)
![Chart.js](https://img.shields.io/badge/chart.js-F5788D.svg?style=for-the-badge&logo=chart.js&logoColor=white)
![RapidAPI](https://img.shields.io/badge/RapidAPI-0055DA?style=for-the-badge&logo=rapid&logoColor=white)

[View Demo] · [Report Bug]

</div>

---

## 📖 Overview
This project serves as a **Data Visualization Dashboard** that fetches live trending topics from Twitter (X) and visualizes them in an interactive bar chart. It is designed to provide a quick snapshot of what is currently viral in specific regions (default: Philippines), helping users analyze social media volume at a glance.

## ✨ Key Features

### 📊 Visualization & UI
* **Interactive Bar Charts:** Powered by **Chart.js**, displaying trend volume with hover effects.
* **Color-Coded Data:** Distinct datasets using RGBA colors for easy distinction between trending topics.
* **Horizontal Layout:** Optimized `indexAxis: 'y'` layout to read long hashtags easily.
* **Dynamic Date Display:** Automatically renders the current date in US format.

### ⚙️ Backend & Logic
* **Live API Integration:** Connects to **Twitter Trends via RapidAPI** using `fetch` and `FormData`.
* **Data Transformation:** Utilizes JavaScript `.map()` and loops to parse raw JSON into consumable chart datasets.
* **Top 25 Filter:** Automatically filters and displays the top 25 highest-volume trends.

---

## 🛠️ Tech Stack

| Component | Technology | Usage |
| :--- | :--- | :--- |
| **Core Logic** | JavaScript (ES6+) | DOM Manipulation, API Fetching, Data Parsing |
| **Visualization** | Chart.js | Rendering the Bar Chart |
| **Data Source** | RapidAPI | Twitter Trends Provider |
| **Styling** | CSS / HTML5 | Layout and Structure |

---

## 🧩 How It Works

1.  **Date Initialization:** The script captures the current user date and formats it.
2.  **API Request:** A `POST` request is sent to RapidAPI with a specific WOEID (Where On Earth ID).
    * *Current WOEID:* `23424934` (Philippines 🇵🇭)
3.  **Data Processing:**
    * The JSON response is parsed.
    * A loop extracts the top 25 trends.
    * `map()` creates parallel arrays for **Topic Names** and **Tweet Volumes**.
4.  **Rendering:** The data is injected into the Chart.js instance to update the DOM.

---

## 🚀 Getting Started

### Prerequisites
* A text editor (VS Code, etc.)
* A generic browser (Chrome, Edge, etc.)
* An API Key from [RapidAPI (Twitter Trends)](https://rapidapi.com/hub)

### Installation

1.  **Clone the repo**
    ```bash
    git clone [https://github.com/yourusername/twitter-visualizer.git](https://github.com/yourusername/twitter-visualizer.git)
    ```
2.  **Set up your API Key**
    Open `script.js` and locate the `options` object:
    ```javascript
    headers: {
        'x-rapidapi-key': 'INSERT_YOUR_RAPIDAPI_KEY
