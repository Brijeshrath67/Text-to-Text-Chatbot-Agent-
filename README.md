This project demonstrates how to build a chatbot agent using the Hugging Face Hub Inference API. The chatbot interacts with users in natural language, remembers previous context, and follows a defined system prompt to behave as a friendly, helpful AI assistant.

📌 Features

Uses Hugging Face InferenceClient for API-based interaction with large language models

Defines a system role prompt to guide chatbot behavior (clear, polite, step-by-step reasoning)

Maintains chat history so the agent remembers past conversation turns

Provides an interactive chat loop for real-time user input and responses

Configurable to work with different Hugging Face models

🛠️ Requirements

Make sure you have the following installed:

Python 3.8+

Hugging Face Hub SDK (huggingface_hub)

(Optional) Jupyter Notebook for running interactively

Install dependencies:
pip install huggingface_hub


⚙️ Setup

1.Get a Hugging Face API token from Hugging Face settings.

2.Replace HF_TOKEN in the notebook with your token:
HF_TOKEN = "your_huggingface_api_token"
client = InferenceClient(token=HF_TOKEN)

3.Choose a model (default: deepseek-ai/DeepSeek-R1-0528):
reply = chat_with_agent("Hello!", model="deepseek-ai/DeepSeek-R1-0528")


▶️ Usage

Run the notebook or Python script:
python Text_to_Text_Chatbot_Agent.py


Example interaction:
🤖 Simple Agent (type 'exit' to quit)
The agent knows its role and remembers context.

You: Hello
Agent: Hi there! How can I help you today?

You: Who created you?
Agent: I was built using Hugging Face’s AI models and a simple Python agent loop.



📂 Project Structure:
├── Text to Text Chatbot_Agent.ipynb   # Jupyter Notebook implementation
├── README.md                          # Documentation


✨ Customization

Modify the system prompt to change the chatbot’s personality.

Swap in other Hugging Face models (e.g., gpt2, meta-llama/Llama-2, mistral, etc.).

Extend the agent with additional features like:

Logging chat history to a file

Adding a web UI (Streamlit/Gradio)

Integrating external knowledge sources

🚀 Future Improvements

Deploy as a web app using Flask, FastAPI, or Streamlit

Add support for voice input/output

Connect with tools and APIs for more powerful agent behavior.
