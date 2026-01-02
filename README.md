# AutoGen WebScrabber 🕷️

A vision-based web scraping tool that uses **AutoGen**, **Puppeteer**, and **GPT-4 Vision** to extract information from websites through visual analysis rather than traditional DOM parsing.

## 🚀 Overview

This project implements a "Vision Crawl" agent. Instead of relying on CSS selectors or XPath, which can break frequently, this tool:
1. Navigates to a URL using Puppeteer.
2. Captures a full-page screenshot.
3. Sends the image to a GPT-4 Vision model via AutoGen.
4. Uses natural language processing to understand and extract data from the visual representation.

## ✨ Features

- **Visual Extraction**: No more brittle selectors. Just ask what you want from the page.
- **Multimodal AI**: Leverages `gpt-4-vision-preview` for high-accuracy visual comprehension.
- **Automated Workflow**: Orchestrated by AutoGen for seamless agent interaction.
- **Full-Page Capture**: Puppeteer ensures the entire page is rendered and captured.
- **Stealth Mode**: Includes `puppeteer-extra-plugin-stealth` to reduce bot detection.

## 🛠️ Prerequisites

- **Python 3.8+**
- **Node.js 16+**
- **OpenAI API Key** (configured with GPT-4 Vision access)

## 📥 Installation

### 1. Clone the repository
```bash
git clone <repository-url>
cd AutoGen_WebScrabber
```

### 2. Install Python dependencies
```bash
pip install -r requirements.txt
```

### 3. Install Node.js dependencies
```bash
npm install
```

## ⚙️ Configuration

Create an `OAI_CONFIG_LIST.json` file in the root directory with your OpenAI API credentials:

```json
[
  {
    "model": "gpt-4-vision-preview",
    "api_key": "YOUR_OPENAI_API_KEY"
  }
]
```

## 🖥️ Usage

Run the main script:
```bash
python vision_crawl.py
```

Follow the prompts:
1. **URL**: Enter the website you want to scrape (e.g., `https://www.amazon.com`).
2. **Goal**: Describe what you want to find (e.g., "List all the products and their prices").
3. **Screenshot Name**: Name the file (e.g., `amazon_prices.jpg`).

## 📂 Project Structure

- `vision_crawl.py`: The main Python entry point using AutoGen.
- `screenshot.js`: Node.js script that handles Puppeteer navigation and screenshots.
- `package.json`: Node dependencies for Puppeteer.
- `requirements.txt`: Python dependencies for AutoGen.
- `OAI_CONFIG_LIST.json`: API configuration (not included in repo).

## 🛡️ License

This project is licensed under the ISC License - see the [package.json](package.json) file for details.
