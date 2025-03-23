# AI Pitch Analysis Model

## Overview
This project implements an **AI-powered Pitch Analysis Model** that evaluates startup pitch decks by extracting key sections and generating a structured analysis. The model uses **OCR/PDF parsing** to extract text, **regular expressions** to identify important sections, and the **Gemini API** to score and provide feedback on each section.

## Features
- **Extracts text from PDF pitch decks** using `PyMuPDF`.
- **Identifies key sections**: Problem, Solution, Market, Business Model, Financials, and Team.
- **Uses LLM (Gemini API)** to evaluate the pitch quality.
- **Generates structured feedback** with strengths, weaknesses, and suggestions for improvement.

## Installation
### Prerequisites
Ensure you have Python installed, then install the required dependencies:
```sh
pip install pymupdf google-generativeai
```

## Usage
### 1. Configure Gemini API
Replace `YOUR_GEMINI_API_KEY` with your actual Gemini API key in the script:
```python
genai.configure(api_key="YOUR_GEMINI_API_KEY")
```

### 2. Run the Script
Ensure you have a pitch deck in PDF format (e.g., `sample_pitch_deck.pdf`) in the working directory, then run:
```sh
python ai_pitch_analysis.py
```

### 3. Output
The script extracts text, identifies sections, and evaluates the pitch. Example output:
```
Extracted Sections: {'Problem': 'The lack of...', 'Solution': 'A web platform...', ...}

AI Feedback:
Overall Score: 75/100
Strengths: Clear problem definition, strong financials.
Weaknesses: Needs better market validation.
```

## File Structure
```
├── ai_pitch_analysis.py  # Main script
├── sample_pitch_deck.pdf # Example pitch deck
├── README.md             # Project documentation
```

## Next Steps
- Improve regex patterns for better text extraction.
- Fine-tune a custom LLM instead of using an API.
- Expand dataset to analyze multiple pitch decks.

## License
This project is open-source and available under the MIT License.

