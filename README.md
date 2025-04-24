# PDF/TXT to PPT Converter

A Python CLI tool that converts PDF or text files to PowerPoint presentations using OpenAI-compatible APIs for content extraction and Llama Cloud for PDF parsing.

## Installation

1. Clone this repository
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Create a `.env` file based on `.env.example` and configure:
```env
OPENAI_API_KEY=your-api-key-here
OPENAI_API_BASE=https://api.together.xyz  # For Together or other compatible APIs
OPENAI_MODEL_NAME=model-name-here         # e.g. deepseek-ai/DeepSeek-V3
LLAMA_CLOUD_API_KEY=your-llama-key-here   # For PDF parsing
```

## Usage

```bash
python app.py input.pdf
# or
python app.py input.txt
```

The tool will:
1. Parse PDF content using Llama Cloud (for PDF files)
2. Extract text from the input file
3. Generate a slide structure using any OpenAI-compatible API
4. Create a PowerPoint presentation (output_YYYYMMDD_HHMMSS.pptx)
5. Display the generated JSON structure

## Requirements

- Python 3.7+
- API keys for:
  - OpenAI or compatible API (Together, etc.)
  - Llama Cloud (for PDF parsing)
- PDF or text file as input

## Notes

- The tool processes the first 3000 characters of input for demo purposes
- Output PPT uses default "Title and Content" layout
- Supports any OpenAI-compatible API endpoint
- Llama Cloud provides high-quality PDF parsing
