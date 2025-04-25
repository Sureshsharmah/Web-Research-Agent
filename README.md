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

Here is the Video link - https://drive.google.com/file/d/1-ekyacQSEQhDatNAzZt9nKOrKAbjMSx8/view?usp=drive_link
