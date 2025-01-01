# RAG AI Chat-Bot

This repository contains a **Retrieval-Augmented Generation (RAG) Chatbot** built with Streamlit, LangChain, and Groq. The chatbot retrieves relevant information from a provided document and generates precise, context-aware answers.

---

## Features

- **Interactive Chat Interface**: Real-time Q&A chatbot powered by advanced language models.
- **Document-Based Retrieval**: Leverages vector embeddings to retrieve context from a document.
- **Streamlined LLM Integration**: Uses Groq models for high-quality natural language generation.
- **PDF Document Support**: Automatically processes PDF documents for context extraction.
- **Persistent Chat History**: Displays historical messages for a seamless user experience.

---

## Project Structure

```
├── .env                 # Environment variables (e.g., GROQ_API_KEY)
├── Pipfile              # Python dependencies and package management
├── Pipfile.lock         # Dependency lock file
├── LICENSE              # License file
├── bot.py               # Main application script
├── Medical_book.pdf       # Sample PDF document for retrieval
├── README.md            # Project documentation
```

---

## Installation

Follow these steps to set up the project on your local machine.

### Prerequisites

- Python 3.9 or later
- Pipenv installed (`pip install pipenv`)
- A valid Groq API key

### Setup Instructions

1. **Clone the Repository**
   ```bash
   git clone https://github.com/sabahatatta/AI-Chat-Bot.git
   cd rag-chatbot
   ```

2. **Install Dependencies**
   Install the required dependencies using Pipenv:
   ```bash
   pipenv install
   ```

3. **Activate the Virtual Environment**
   ```bash
   pipenv shell
   ```

4. **Set Up the API Key**
   Add your Groq API key to an `.env` file in the project root or export it as an environment variable:
   ```
   GROQ_API_KEY=your_api_key
   ```

5. **Add Your Document**
   Replace `Medical_book.pdf` with your own PDF file or keep the sample file for testing.

6. **Run the Application**
   Start the chatbot by running:
   ```bash
   streamlit run bot.py
   ```

7. Open the URL provided by Streamlit in your browser to start using the chatbot.

---

## Usage

1. Once the chatbot is running, enter a query in the input field.
2. The chatbot will retrieve relevant information from the provided PDF and generate an accurate answer.
3. Historical messages will be displayed for reference.

---

## Customization

### Replace the Document
To use your own document, replace `Medical_book.pdf` with your PDF file in the project directory.

### Modify the Language Model
Update the `model_name` parameter in the `ChatGroq` initialization to use a different Groq model:
```python
model="your_preferred_model_name"
```

### Adjust Chunking
Fine-tune the `chunk_size` and `chunk_overlap` in `RecursiveCharacterTextSplitter` to optimize text chunking.

---

## Troubleshooting

- **Failed to Load Document**  
  Ensure the PDF file is in the project directory and readable by the script.

- **Missing GROQ_API_KEY**  
  Verify that the `GROQ_API_KEY` is set in your `.env` file or exported as an environment variable.

- **Pipenv Issues**  
  If you encounter Pipenv-related errors, try:
  ```bash
  pipenv install --skip-lock
  ```

---

## Contribution

Contributions are welcome! If you have suggestions, issues, or improvements, feel free to open a pull request or issue.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

---


