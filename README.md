# Mistral-Powered-URL-Summarizer-Hugging-Face-LangChain

This Streamlit application allows you to summarize content from YouTube videos or website URLs using LangChain and the Hugging Face Inference API, specifically the Mistral 7B Instruct model.

## Features

* **YouTube Video Summarization:** Extracts and summarizes transcripts from YouTube videos.
* **Website URL Summarization:** Extracts and summarizes text content from website URLs.
* **Hugging Face Inference API:** Leverages the Mistral 7B Instruct model for accurate and efficient summarization.
* **LangChain Integration:** Utilizes LangChain for document loading and summarization chains.
* **User-Friendly Interface:** Built with Streamlit for easy interaction.
* **Error Handling:** Robust error handling for invalid URLs and YouTube loading issues.

## Getting Started

### Prerequisites

* Python 3.7+
* A Hugging Face API key (Sign up at [Hugging Face](https://huggingface.co/))
* Internet connection

### Installation

1.  **Clone the repository**

2.  **Create a virtual environment (recommended)**

3.  **Install dependencies:**

    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the application:**

    ```bash
    streamlit run app.py
    ```

### Usage

1.  **Enter Hugging Face API Key:**
    * In the sidebar, enter your Hugging Face API key.
2.  **Enter URL:**
    * In the main interface, enter the YouTube video URL or website URL you want to summarize.
3.  **Summarize:**
    * Click the "Summarize the content from YT Or Website" button.
4.  **View Summary:**
    * The summarized content will be displayed on the screen.

### Code Explanation

* **`app.py`:**
    * This file contains the Streamlit application and the LangChain summarization logic.
    * It handles URL input, Hugging Face Inference API integration, and error handling.
    * It uses `YoutubeLoader` and `UnstructuredURLLoader` to load content.
    * Uses LangChain's `load_summarize_chain` to summarize the data.

### Dependencies

* `streamlit`
* `langchain`
* `langchain-huggingface`
* `langchain-community`
* `validators`
* `pytube`

### Error Handling

The application includes robust error handling to manage:

* Invalid URLs.
* Issues loading YouTube videos (e.g., unavailable videos, network errors).
* General Exceptions.
