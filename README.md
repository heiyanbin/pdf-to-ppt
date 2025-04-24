# PDF/TXT to PPT Converter

A Python CLI tool that converts PDF or text files to PowerPoint presentations using OpenAI for content extraction.

## Installation

1. Clone this repository
2. Install dependencies:
```bash
pip install -r requirements.txt
```
3. Create a `.env` file and add your OpenAI API key:
```env
OPENAI_API_KEY=your-api-key-here
```

## Usage

```bash
python app.py input.pdf
# or
python app.py input.txt
```

The tool will:
1. Extract text from the input file
2. Generate a slide structure using OpenAI
3. Create a PowerPoint presentation (output_YYYYMMDD_HHMMSS.pptx)
4. Display the generated JSON structure

## Requirements

- Python 3.7+
- OpenAI API key
- PDF or text file as input

## Notes

- The tool processes the first 3000 characters of input for demo purposes
- Output PPT uses default "Title and Content" layout
- Ensure your OpenAI API key has sufficient credits
