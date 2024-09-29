# TamilNadu Scheme Connect

**Tamil Nadu Scheme Connect** is a web application that provides quick access detailed information on Tamil Nadu's government services and schemes. It efficiently indexes official documents for quick data retrieval and uses a multilingual chat interface with translation support to deliver accurate responses based on official government information.

## Overview

Built with **Flask**, **JavaScript**, **CSS**, and **HTML**, the application provides detailed information about government schemes and services in Tamil Nadu. **Tamil Nadu Scheme Connect** combines document indexing, query processing, and translation to deliver accurate responses to user queries.

## Features

- **Document Indexing**: Indexes documents for efficient search and retrieval using a vector database.
- **Query Handling**: Processes user queries to extract meaningful information from indexed documents.
- **Language Translation**: Supports Tamil, Hindi, and English to cater to a diverse user base.
- **Google API Integration**: Locates nearby NGOs, hospitals, and blood donation camps from users location
- **News API Integration**: Retrieves and displays news on topics like legal matters, women empowerment, and welfare.
- **Voice Input**: Allows users to interact with the chatbot using voice commands.

## How It Works

1. #### Document Indexing:
   - The application loads and indexes documents from the `./hack4` directory.
   - Uses a sentence splitter to create nodes and a vector store index for document retrieval.
   - Persists the index in the `./index_store_final/vector` directory for future use.

2. #### Query Processing:
   - User queries are processed by the **OpenAIAgent**, leveraging a vector query engine to provide detailed responses based on indexed documents.
   - Additional information is retrieved from Tamil Nadu government websites using the **TavilySearchAPIRetriever**.

3. #### Google API Integration:
   - Locates nearby NGOs, hospitals, and blood donation camps based on user location queries.

4. #### News API:
   - Fetches and displays news articles related to legal topics, women empowerment, welfare, and more.

5. #### Language Translation:
   - Supports Tamil, Hindi, and English, allowing seamless language switching.

6. #### Voice Input:
   - Allows users to engage with the chatbot using voice commands for a more user-friendly experience.


## File Structure

- `chatbot_app.py`: Main Flask application file.
- `app(streamlit).py`: Main Streamlit application file.
- `./hack4/`: Directory containing PDF documents for indexing (excluded due to proprietary data).
- `./index_store_final/`: Directory for storing the vector index (`vector.zip` available in Google Drive link below).
- `venv/`: (Optional) Environment variables file.
- `requirements.txt`: List of dependencies.
- `templates/`: Contains HTML templates such as `chatbot.html`, `index.html`, `login.html`, `map.html`, `newsmain.html`.
- `static/`: Contains JavaScript and CSS files such as `mapscripts.js`, `mapstyles.css`, `newsscripts.js`, `newsstyles.css`, `scripts.js`, `styles.css`.

## Dependencies

- **Flask**: For backend development.
- **JavaScript, CSS, HTML**: For frontend development.
- **Google API**: For locating nearby NGOs, hospitals, and blood donation camps.
- **News API**: For fetching news articles.
- **langchain_community**: For API retrieval and document processing.
- **llama_index**: For document indexing and query processing.
- **dotenv**: For managing environment variables.

## Additional Resources

For convenience, you can download the indexed documents from the following Google Drive link: [Indexed Documents](https://drive.google.com/drive/folders/1X5AOffQVnzLr7H-8lfTrlOQuKWxrTcjT?usp=sharing)


## Contact

For any questions or issues, feel free to reach out:

- **lakshanikasekhar.pro@gmail.com**
- **sansitakarthik2005@gmail.com**
- **karthikapanchu2004@gmail.com**
- **vaadhishree@gmail.com**

---

Thank you for using **Tamil Nadu Scheme Connect**!
