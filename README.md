
# Gemini Pro Chatbot

This project is a simple chatbot application built using **Streamlit** and **Google Gemini-Pro AI**. The chatbot leverages Google’s Gemini-Pro AI model for generating responses based on user input, and the conversation is displayed interactively on a web interface.

## Features

- Chat with Gemini Pro AI using a simple Streamlit interface.
- Displays chat history between the user and the assistant.
- Real-time interaction using Google Gemini-Pro model.
- User can send questions and get AI-generated responses.

## Prerequisites

Before running the app, make sure you have the following installed:

- **Python 3.7+**
- **Google Gemini API Key**: You need a valid Google Gemini API key to access the AI model.

## Installation

### 1. Clone the repository

First, clone this repository to your local machine:

```bash
git clone https://github.com/your-username/gemini-chatbot.git
cd gemini-chatbot
```

### 2. Set up a virtual environment (optional but recommended)

Create a virtual environment and activate it:

For Windows:
```bash
python -m venv .venv
.venv\Scripts\activate
```

For macOS/Linux:
```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install dependencies

Install the required Python packages:

```bash
pip install -r requirements.txt
```

### 4. Add your Google Gemini API Key

In `main.py`, replace the placeholder value of `GOOGLE_API_KEY` with your actual Google Gemini API key:

```python
GOOGLE_API_KEY = "YOUR_GOOGLE_API_KEY"
```

Alternatively, you can set the API key as an environment variable:

```bash
export GOOGLE_API_KEY="YOUR_GOOGLE_API_KEY"  # macOS/Linux
set GOOGLE_API_KEY="YOUR_GOOGLE_API_KEY"     # Windows
```

### 5. Run the Streamlit app

Once everything is set up, you can start the Streamlit app:

```bash
streamlit run main.py
```

This will launch the chatbot in your browser. You can interact with the Gemini Pro AI model by typing questions into the input field.

## How It Works

1. **Google Gemini Integration**: The app integrates with the Google Gemini-Pro AI model using the `google.generativeai` Python library. The app is initialized with the API key to authenticate and connect to the Gemini model.
   
2. **Streamlit Interface**: The app uses Streamlit to provide a web-based chat interface, where users can input text and view the AI's responses in real-time.

3. **Session Management**: The app stores the chat session state in `st.session_state` to preserve the conversation history. This allows users to continue their chat even after interacting with the model multiple times.

4. **Translation of Roles**: The app translates the roles used by Gemini-Pro (like "model") into Streamlit-friendly terms (e.g., "assistant") to ensure the correct display of chat messages.

## Customization

- **Change the Page Title/Icon**: Modify the `st.set_page_config()` method to customize the page title and icon.
  
- **Update the Chatbot’s Name**: You can change the chatbot’s title by modifying the string in the `st.title()` function.

## Troubleshooting

### 1. **Access Denied on Running the App**:
If you encounter permission issues when running `streamlit run main.py`, try running the terminal or command prompt as **Administrator**.

### 2. **Streamlit Session State Issue**:
Make sure you are running the app using `streamlit run main.py` and not directly with `python main.py`. Session state only works with Streamlit's server.

### 3. **API Key Issues**:
If you receive an error related to the API key, ensure that your API key is valid and correctly placed in the script or set as an environment variable.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgements

- **Streamlit**: https://streamlit.io/
- **Google Gemini API**: https://developers.google.com/generative-ai
