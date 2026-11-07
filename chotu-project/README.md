# Smart Document Summarizer + Chotu

Upload a PDF / DOCX / TXT / image / scanned PDF, get a summary in your language, ask questions,
listen to it, copy it, and save it as a PDF. Plus **Chotu**, a voice-enabled helper for farming,
animals, health and daily life.

## Run
1. Install Python 3.10+ and Tesseract OCR (with Hindi/Telugu/Tamil language packs).
   - Ubuntu: `sudo apt install tesseract-ocr tesseract-ocr-hin tesseract-ocr-tel tesseract-ocr-tam`
2. `cd backend && pip install -r requirements.txt`
3. Set your key: `export ANTHROPIC_API_KEY=your-key` (Windows: `set ANTHROPIC_API_KEY=your-key`)
4. `uvicorn main:app --reload` then open http://localhost:8000

## Features
- Files: PDF, DOCX, TXT, images, scanned PDFs (OCR). 10 MB limit, clear errors.
- Long documents are split into chunks and combined.
- Styles: short, detailed, bullets, important points only.
- Auto document type: resume feedback, contract key terms, simple paper explanation.
- Output language selector, ask questions about the document, listen (text-to-speech).
- Copy, and Download PDF (uses the browser's Save as PDF so every Indian script renders correctly).
- Chotu: chat with memory, voice in/out, photo upload, same-language replies, safety rules.
- Privacy: files are read in memory and never saved. API key stays on the backend. Rate limit: 10-20 requests/min per IP.
- Prompt-injection guard: document text is treated as data.

## Not built yet (next versions)
Live weather / mandi prices / scheme data, ICAR knowledge base, WhatsApp, login + history.
