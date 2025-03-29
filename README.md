🌐 DeepTrace

📌 Overview

This project is an asynchronous web crawler designed for scraping data from websites on the Tor (.onion) and I2P (.i2p) networks. Additionally, it features an NLP-based hate speech classification system for analyzing extracted text data.

🚀 Features

🔹 Asynchronous Web Crawling

✅ Concurrent crawling of Tor and I2P websites using asyncio and aiohttp.
✅ Data is saved as HTML files in the archive/ directory.
✅ CSV log (data.csv) tracks URLs and timestamps.
✅ Avoid redundant crawling by storing temporary URLs in temp/scraped.txt.

🔹 Randomization & Security

🔒 Random User-Agents for enhanced anonymity.
🔒 Secure random strings used for various purposes.

🔹 NLP-Based Hate Speech Analysis

🧠 Utilizes pre-trained NLP model: Hate-speech-CNERG/dehatebert-mono-english.
📊 Performs automated hate speech classification on extracted text.

🔹 User-Friendly CLI Interface

🖥️ main.py provides an interactive menu for:

Starting web crawling on Tor, I2P, or both.

Checking the Tor IP Address.

🔹 Continuous Background Processing

♻️ Runs a background thread (run_process_files_continuously) for automated file processing.

⚙️ Prerequisites

📌 Python 3.10.x is recommended.
📌 Install dependencies:

pip install -r requirements.txt

📌 Ensure Tor is running and configured for web crawling through the Tor network.

🛠️ Usage

▶️ Run the CLI:

python main.py

🎯 Choose from the menu to start crawling Tor, I2P, or both.
▶️ Run individual crawlers:

python async_crawl4.py    # For Tor
python async_crawl_i2p.py # For I2P

♻️ Background file processing is handled automatically.

📂 Project Structure

📁 Project Root
│── async_crawl4.py       # Tor Network Crawler
│── async_crawl_i2p.py    # I2P Network Crawler
│── main.py               # CLI for user interaction
│── nlp_main.py           # Hate Speech Classification
│── requirements.txt      # Dependencies
│── temp/                 # Temporary storage
└── archive/              # Scraped data storage

🙌 Acknowledgements

✨ Built with:

transformers library by Hugging Face 🧠

Pre-trained model: Hate-speech-CNERG/dehatebert-mono-english

📢 Disclaimer: This project is intended strictly for ethical research and educational purposes. Users are responsible for ensuring compliance with relevant laws and regulations.
