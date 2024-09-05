

---

# **DocuSummarizeAI: Unstructured Document Content Extraction and Summarization**

## Overview
**DocuSummarizeAI** is a comprehensive system designed to automatically extract and generate various forms of content from unstructured documents like PowerPoint presentations (PPT), Word documents (DOC), and PDFs. This solution leverages advanced AI-driven algorithms to analyze text, tables, images, and graphs and produce summaries in the form of short descriptions, long descriptions, voice-overs, and elevator pitches.

The platform streamlines the process of summarizing and presenting key information from large documents, making it particularly useful for businesses, educational institutions, and content creators who need quick access to summarized content without manually reading and analyzing entire documents.

## Key Features
- **Content Extraction**: Extracts text, tables, images, and graphs from various document formats (PPT, DOC, PDF).
- **Summarization Types**:
  - **Elevator Pitch**: Concise, compelling summaries ideal for quick presentations.
  - **Short Description**: Brief overviews that highlight key points.
  - **Long Description**: Comprehensive summaries that cover all aspects of the document.
  - **Voice-Over Script**: Engaging scripts suitable for explainer videos or narrated presentations.
- **AI-powered Analysis**: Utilizes OpenAI’s GPT-4 and Google Gemini Pro Vision for intelligent content analysis and summarization.
- **Efficient Information Retrieval**: Helps users access summarized and detailed content quickly.
- **API Integration**: Deployed APIs using FastAPI for live use in various applications.

## System Architecture
The core functionality of **DocuSummarizeAI** revolves around two main components:
1. **Text and Table Extraction**: Extracts textual data and tables from documents and summarizes them using OpenAI’s GPT-4-turbo model.
2. **Image and Graph Analysis**: Uses Google Gemini Pro Vision to analyze images and graphs, providing intelligent descriptions of visual data.

### Cost Optimization
The solution is designed with cost-efficiency in mind, with pricing calculations for both OpenAI and Google Gemini APIs. It includes dynamic cost estimation based on token usage, ensuring users are aware of API costs upfront.

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/yourusername/DocuSummarizeAI.git
   cd DocuSummarizeAI
   ```

2. **Set up a virtual environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # For Windows use venv\Scripts\activate
   ```

3. **Install dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up environment variables**:
   Create a `.env` file in the root directory and add your OpenAI and Google API keys:
   ```
   OPENAI_API_KEY=your_openai_api_key
   GOOGLE_API_KEY=your_google_api_key
   ```

5. **Run the FastAPI application**:
   ```bash
   uvicorn app:app --reload
   ```

## Usage

### API Endpoints
- **Upload PPT for Processing**:
  - `POST /upload_ppt/`
  - Upload a PowerPoint file for extraction and summarization.

- **Generate Elevator Pitch**:
  - `POST /elevator_pitch/`
  - Upload a document and get a concise elevator pitch.

- **Generate Short Description**:
  - `POST /short_description/`
  - Upload a document and get a brief overview of the content.

- **Generate Long Description**:
  - `POST /long_description/`
  - Upload a document and get a comprehensive description.

- **Generate Voice-Over Script**:
  - `POST /voice_over/`
  - Upload a document and get a voice-over script.

## Technologies Used
- **FastAPI**: For creating and deploying the RESTful APIs.
- **OpenAI GPT-4**: For generating summaries and descriptions.
- **Google Gemini Pro Vision**: For analyzing and summarizing visual content like images and graphs.
- **Python-PPTX**: For extracting content from PowerPoint files.
- **Pillow (PIL)**: For image processing and analysis.

---
