# Founder-Investor Matching AI Model

## Overview
This project implements an **AI-driven Founder-Investor Matching Model** that analyzes structured startup data and investor preferences to generate a **match score** between founders and investors. The model also integrates **Google Gemini AI** to provide insights on funding strategies.

## Features
- **Processes structured investor and founder data** to find compatibility.
- **Extracts and preprocesses investment preferences** from JSON data.
- **Calculates a match score** based on industry, stage, and funding requirements.
- **Integrates Google Gemini AI (gemini-1.5-pro)** for expert funding insights.
- **Ranks and displays the top investors** based on the match score.

## Installation
### Prerequisites
Ensure you have Python installed and install the required dependencies:
```sh
pip install pandas google-generativeai
```

## Usage
### 1. Configure Gemini API
Replace `YOUR_GEMINI_API_KEY` with your actual Gemini API key in the script:
```python
genai.configure(api_key="YOUR_GEMINI_API_KEY")
```

### 2. Run the Script
Ensure you have an investor dataset (`Combined file.xlsx - Sheet1.json`) in the working directory. Then, run:
```sh
python founder_investor_matching.py
```

### 3. Output
The script will output the **top-matching investors** and **AI-generated funding insights**. Example:
```
Top Investors:
Name          | Industry | Stage | Cheque Range | Match Score
------------------------------------------------------------
Investor A    | Fintech | Seed  | $50K - $500K | 100
Investor B    | Fintech | Seed  | $100K - $1M  | 100
...

🔹 Gemini AI Insights:
"For a Fintech startup at the Seed stage requiring $500,000, consider angel investors, pre-seed VC funds, and government grants. Ensure you highlight traction and market size..."
```

## File Structure
```
├── founder_investor_matching.py  # Main script
├── Combined file.xlsx - Sheet1.json  # Sample dataset
├── README.md                      # Documentation
```

## Next Steps
- Enhance investor ranking by incorporating additional factors like location and previous investments.
- Optimize funding strategy insights using fine-tuned models.
- Expand compatibility scoring with NLP-based investor preference analysis.

## License
This project is open-source and available under the MIT License.

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

