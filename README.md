
# News Research Tool 📈

A Streamlit-based news research tool that uses LangChain and OpenAI to process news articles from URLs and answer questions based on the content.

## Features

- Load and process news articles from multiple URLs
- Extract and split text content using LangChain
- Create embeddings using OpenAI
- Store vectors in FAISS for efficient retrieval
- Answer questions based on the processed content
- Display sources for answers

## Recent Fixes

The following issues have been resolved:

1. **Import Errors**: Updated all LangChain imports to use the correct module structure:
   - Changed `from langchain import OpenAI` to `from langchain_openai import OpenAI`
   - Updated document loaders, embeddings, and vectorstores to use `langchain_community`
   - Fixed deprecated import warnings

2. **Package Compatibility**: Updated `requirements.txt` with compatible versions:
   - LangChain 0.3.27
   - LangChain Community 0.3.27
   - LangChain OpenAI 0.3.29
   - Updated all dependencies to compatible versions

3. **Dependency Conflicts**: Resolved version conflicts between packages by using compatible versions

## Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd 2_news_research_tool_project
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Set up your OpenAI API key:
   - Create a `.env` file in the project root
   - Add your OpenAI API key: `OPENAI_API_KEY=your_api_key_here`

## Usage

1. Run the Streamlit application:
```bash
streamlit run main.py
```

2. Open your browser and navigate to the provided URL (usually `http://localhost:8501`)

3. Enter news article URLs in the sidebar (up to 3 URLs)

4. Click "Process URLs" to load and process the articles

5. Ask questions in the text input field to get answers based on the processed content

## Testing

To verify that all imports work correctly, run:
```bash
python test_imports.py
```

This will test all the imports used in the main application and confirm everything is working properly.

## Requirements

- Python 3.12+
- OpenAI API key
- Internet connection for loading news articles

## Dependencies

- langchain==0.3.27
- langchain-community==0.3.27
- langchain-openai==0.3.29
- streamlit==1.28.0
- openai==1.99.6
- faiss-cpu==1.11.0.post1
- unstructured==0.18.11
- tiktoken==0.11.0
- python-dotenv==1.0.0

## Troubleshooting

If you encounter any issues:

1. Make sure all dependencies are installed correctly
2. Verify your OpenAI API key is set in the `.env` file
3. Check that you have a stable internet connection
4. Run the test script to verify imports: `python test_imports.py`

## License

This project is open source and available under the MIT License.