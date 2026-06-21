# TalentPulse

TalentPulse is an AI-powered CRM and ATS (Applicant Tracking System) built to manage leads, candidates, tickets, and internal data with an intelligent AI assistant. 

## Features

- **AI Chat & RAG**: Intelligent chatbot powered by Groq (Llama-3) capable of semantic search on uploaded documents (PDFs, Word, TXT, CSV) using FAISS and Sentence Transformers.
- **Automated Resume Parsing**: Upload resumes (PDF/Image) to extract key candidate information automatically using AI and store them in the candidate dataset.
- **Intent Routing**: The AI detects user intent and seamlessly triggers corresponding CRM actions or answers questions from documentation.
- **CRM Management**: Comprehensive management of leads, candidates, support tickets, and reminders.
- **Modern UI**: Next.js 16 Frontend styled with Tailwind CSS v4, utilizing Framer Motion for smooth animations and Recharts for interactive data visualization.

## Tech Stack

### Frontend (`talent_pluse_frontend`)
- **Framework**: Next.js 16 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS v4
- **Libraries**: Framer Motion, Recharts, Lucide React, React Markdown

### Backend (`talent_pluse_backend`)
- **Framework**: FastAPI (API Server) & Django ORM (Database Management)
- **Language**: Python
- **AI / NLP**: Groq LLM API, FAISS, Sentence Transformers, NLTK/Scikit-learn (TF-IDF)
- **Data Processing**: Pandas, pdfplumber, python-docx, BeautifulSoup4

## Project Structure

- `talent_pluse_frontend/`: Contains the Next.js frontend application (Dashboard, Security, Vision, Infrastructure).
- `talent_pluse_backend/`: Contains the Python backend application. Handles routing, API logic, database interactions, and the AI/RAG engine.

## Getting Started

### Prerequisites
- Node.js (v18+)
- Python (3.9+)

### Frontend Setup

1. Navigate to the frontend directory:
   ```bash
   cd talent_pluse_frontend
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Set up environment variables (if any) in `.env.local`.
4. Run the development server:
   ```bash
   npm run dev
   ```
   The frontend will be accessible at `http://localhost:1432`.

### Backend Setup

1. Navigate to the backend directory:
   ```bash
   cd talent_pluse_backend
   ```
2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   # On macOS/Linux:
   source venv/bin/activate
   # On Windows:
   venv\Scripts\activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Configure environment variables: 
   Copy `.env.example` to `.env` and fill in the required keys, especially `GROQ_API_KEY`.
   ```bash
   cp .env.example .env
   ```
5. Apply database migrations (Django):
   ```bash
   python main.py  # First run usually triggers setup, or you can run standard django migrate scripts if configured
   ```
6. Run the backend server:
   ```bash
   python main.py
   ```
   The backend API will be accessible at `http://localhost:8028`. You can view the API documentation at `http://localhost:8028/docs`.

## License
MIT License
