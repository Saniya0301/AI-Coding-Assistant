# AI Coding Assistant

An automated AI-powered coding assistant that extracts coding problems from images, generates Python solutions using a large language model (LLM), and executes the generated code in a secure sandbox environment.

---

## Features

- **OCR Text Extraction:** Uses Tesseract OCR to extract problem descriptions from images.
- **AI Code Generation:** Utilizes Groq LLM (`llama-3.3-70b-versatile` model) via the `agno-agent` package to generate Python code solutions from extracted text.
- **Code Execution Sandbox:** Runs generated Python code safely in an isolated sandbox environment (`E2B Sandbox`).
- **Error Handling:** Automatically explains Python execution errors using the AI model to help debugging.
- **Markdown Code Parsing:** Extracts executable Python code blocks from the AI-generated markdown responses.

---

## Requirements

- Python 3.8+
- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract) installed and configured
- Packages:
  - `pillow`
  - `pytesseract`
  - `agno`
  - `e2b_code_interpreter`
  - `python-dotenv`

Install Python dependencies with:

## Usage

1. Place your problem image (e.g., `test_question.png`) in the project directory.
2. Run the assistant:

3. 3. The assistant will:
- Extract problem text from the image.
- Generate a Python solution using the AI model.
- Execute the code in the sandbox.
- Display the output or provide error explanations.

---

## How It Works

1. **Image OCR:** Extract problem description text.
2. **LLM Prompting:** Send extracted text to Groq LLM to generate Python code.
3. **Code Extraction:** Parse Python code out of LLM markdown output.
4. **Execution:** Run the generated code in E2B sandbox.
5. **Error Handling:** If execution fails, request error explanation from the AI.

---

## Customization

- Modify the `image_path` variable to point to different problem screenshots.
- Change the AI model or parameters in the `Agent` initialization.
- Extend error handling or logging as needed.

---

## License

MIT License

---

## Acknowledgments

- [Tesseract OCR](https://github.com/tesseract-ocr/tesseract)
- [Groq AI](https://www.groq.com/)
- [E2B Code Interpreter](https://github.com/e2b-dev/code-interpreter)

---
