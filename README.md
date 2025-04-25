# Web-Research-Agent

How I Built It
This project was crafted as a dual-agent AI research assistant, built from scratch using cutting-edge tools from the LangChain ecosystem. Here's how I developed it:

🔍 Custom Web Scraping Agent (Tavily): I integrated the Tavily API to fetch structured and relevant web content for any user-defined query. The agent dynamically adjusts search breadth based on the depth of research selected.

🧠 LLM-Powered Drafting Agent (OpenRouter): I built a powerful drafting module using OpenRouter’s Dolphin model via LangChain. It transforms raw research into structured summaries with sections like Key Findings, Analysis, and Conclusion — customizable in tone, length, citation style, and language.

🔄 LangGraph Workflow Pipeline: Using LangGraph, I orchestrated a robust state-based workflow that passes data between agents in a logical sequence, supporting both quick overviews and deep-dive research papers.

🖥️ Interactive UI with Streamlit: The front end was developed in Streamlit with rich UI features, including a dark theme, sidebar settings, PDF/Word export, and real-time API status monitoring.

💾 Caching & Retry Handling: I implemented joblib caching and built-in retry logic (using tenacity) to enhance performance and fault tolerance during API interactions.

📄 Multi-Format Report Generator: Leveraging ReportLab and python-docx, I enabled export to PDF, Word, Markdown, and plain text, maintaining proper academic formatting with pagination, references, and styles.

✨ User-Centric Enhancements: From writing-style previews to responsive download options and inline citation previews, I focused on creating a smooth, informative user experience.

# Web Research Agent

## Overview

A dual-agent system for deep research, powered by OpenAI and Tavily for web crawling and OpenRouter for drafting structured summaries. Built using LangChain, LangGraph, and Streamlit for a seamless and interactive research experience.


## Watch the Demo

[![Watch the demo video](https://drive.google.com/file/d/1-ekyacQSEQhDatNAzZt9nKOrKAbjMSx8/view?usp=drive_link)]


## Setup

1. Clone the repo:

    ``` bash
    git clone https://github.com/Sureshsharmah/Web-Research-Agent
    cd Web-Research-Agent
   ```

2. Install dependencies:

   ``` pip install -r requirements.txt ```

      Ensure you have Python 3.8+ installed. The `requirements.txt` file includes:
   - `langchain-openai`
   - `langchain`
   - `langgraph`
   - `streamlit`
   - `tavily-python`
   - `requests`
   - `tenacity`
   - `python-dotenv`
   - `python-docx`
   - `reportlab`
   - `joblib`


   - Additional dependencies for document processing

3. Create a `.env` file with API keys:

      ```bash
      OPEN_API_KEY=your_open_api_key
      TAVILY_API_KEY=your_tavily_key
      OPENROUTER_API_KEY=your_openrouter_key
      ```
      - Obtained a OpenAPI key from [OpenAI](https://platform.openai.com/docs/api-reference/introduction)
      - Obtain a Tavily API key from [Tavily](https://tavily.com) (free tier available).
      - Obtain an OpenRouter API key from [OpenRouter](https://openrouter.ai) (uses the free models, can be altered as per preference).

4. Run the app locally:

      ```streamlit run app.py```

## Features

- **Dual-Agent System**:
  - **Research Agent**: Fetches data from the web using Tavily, returning structured results (title, content, URL).
  - **Draft Agent**: Generates structured summaries with sections: Research Summary, Key Findings, Analysis, and Conclusion, using LLM model.
- **Customizable Settings**:
  - Writing styles (Academic, Casual, Technical, etc.)
  - Citation formats (APA, MLA, IEEE)
  - Target word count
  - Multiple output formats (PDF, Word, Markdown, Text)
- **Structured Summaries**: Outputs summaries with clear sections (Research Summary, Key Findings, Analysis, Conclusion) for readability.
- **PDF Report Download**: Allows users to download a PDF report containing the query, research data, and structured summary, with proper text wrapping and multi-page support.
- **Retry Logic**: Handles API failures with `tenacity`, retrying up to 3 times with a 2-second delay.
- **OpenRouter Status**: Displays real-time API status in the sidebar, alerting users if OpenRouter is unavailable.
- **Progress Indicator**: Shows a progress bar during research and drafting for better user experience.
- **User Feedback**: Includes a feedback form in the sidebar to collect user suggestions.
- **Custom Styling**: Features high-contrast colors, proper spacing, and readable typography for an enhanced UI.

## Deployment

The application is deployed on Streamlit.


## Usage

1. Visit the [live demo](https://drive.google.com/file/d/1-ekyacQSEQhDatNAzZt9nKOrKAbjMSx8/view?usp=drive_link) or run locally
2. Enter a research query (e.g., "Data Science and Artificial Intelligence")
3. Customize research settings (optional)
4. Click "Run Research" to fetch data and generate a summary
5. View the research data and structured summary
6. Download the report in your preferred format
7. Provide feedback via the sidebar form (optional)




Here is the Video link - https://drive.google.com/file/d/1-ekyacQSEQhDatNAzZt9nKOrKAbjMSx8/view?usp=drive_link
