# MisogiAI Interactive Prompt Playground

An interactive web application that allows users to experiment with different parameters for generating product descriptions using OpenAI's GPT models.

## Features

- Model Selection: Choose between GPT-3.5 Turbo and GPT-4
- Parameter Control:
  - Temperature (0.0 - 1.2)
  - Max Tokens (50 - 300)
  - Presence Penalty (0.0 - 1.5)
  - Frequency Penalty (0.0 - 1.5)
- Custom System and User Prompts
- Stop Sequence Configuration
- Grid View of Results
- Parameter Impact Analysis

## Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/yourusername/MisogiAI-interactive-prompt-playground.git
cd MisogiAI-interactive-prompt-playground
```

2. Create a virtual environment and activate it:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Create a `.env` file in the root directory and add your OpenAI API key:
```
OPENAI_API_KEY=your_api_key_here
```

5. Run the application:
```bash
python app.py
```

6. Open your browser and navigate to `http://localhost:5000`

## Usage

1. Select your desired model (GPT-3.5 Turbo or GPT-4)
2. Enter your system prompt and user prompt
3. Adjust the parameters:
   - Temperature: Controls randomness (0.0 = deterministic, 1.2 = more creative)
   - Max Tokens: Maximum length of the generated response
   - Presence Penalty: Reduces repetition of topics
   - Frequency Penalty: Reduces repetition of words
4. Add any stop sequences if needed
5. Click "Generate" to see results across different parameter combinations

## Parameter Impact Analysis

The playground allows you to observe how different parameters affect the generated product descriptions:

- **Temperature**: Higher values (e.g., 1.2) produce more creative and varied descriptions, while lower values (e.g., 0.0) generate more consistent and focused outputs.
- **Max Tokens**: Controls the length of the description. Lower values (50) produce concise descriptions, while higher values (300) allow for more detailed and comprehensive content.
- **Presence Penalty**: Higher values (1.5) encourage the model to discuss different aspects of the product, while lower values (0.0) may lead to repetitive content.
- **Frequency Penalty**: Higher values (1.5) promote vocabulary diversity, while lower values (0.0) may result in repeated word usage.
