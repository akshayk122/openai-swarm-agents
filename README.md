
### My Search Assistant 🔎

This project provides a web-based application built with **Streamlit** that leverages several AI agents to perform web research, analysis, and article generation. Users can search the web, analyze results, and generate a polished article on any given topic.

### Features 🌟:
- **Web Search:** 🔍 Uses DuckDuckGo's search capabilities to fetch the latest news and articles based on the user's query.
- **Research Analysis:** 🧠 Analyzes the raw search results, removes duplicates, synthesizes information, and verifies consistency across sources.
- **Article Generation:** ✍️ Transforms the analyzed data into a professional, polished article ready for publication.
- **Real-time Streaming:** ⚡ Streams the article generation process in real-time for a smooth user experience.

### Technologies 💻:
- **Streamlit:** 🎨 For creating the interactive web interface.
- **Swarm:** 🤖 To manage and run multiple AI agents.
- **DuckDuckGo Search (via `duckduckgo_search` Python library):** 🌐 To fetch the latest search results from DuckDuckGo.
- **OpenAI or similar models:** 💬 For natural language processing tasks such as web search, analysis, and writing.
- **dotenv:** 🔒 For managing environment variables securely.

### Setup & Installation 🚀

#### Prerequisites:
- Python 3.7 or higher 🐍
- OpenAI or similar NLP model (e.g., `llama3.2` or other compatible models)
- The `duckduckgo_search` library for fetching search results.

#### Step 1: Clone the repository

```bash
git clone https://github.com/yourusername/internet-research-assistant.git
cd internet-research-assistant
```

#### Step 2: Install the dependencies

Create a Python virtual environment (recommended) and install the required libraries:

```bash
pip install -r requirements.txt
```

#### Step 3: Set up environment variables

Create a `.env` file in the root directory of the project and include any necessary API keys (e.g., OpenAI API key) URL for Ollama server if you're running it locally:

```text
OPENAI_API_KEY=your_openai_api_key_here
```
or 

```text
OPENAI_BASE_URL=http://localhost:11434/v1
OPENAI_API_KEY=fake-key
```

#### Step 4: Run the Streamlit app

Launch the application with the following command:

```bash
streamlit run app.py
```

This will start the app in your web browser, and you can begin entering search queries to generate articles.

### How It Works 🛠️:

1. **Search Query:** 🧐 The user enters a search query.
2. **Web Search:** 🌍 The web search agent queries DuckDuckGo using the `duckduckgo_search` library to retrieve the latest articles and news related to the query.
3. **Analysis:** 🔎 The raw search results are sent to the research analysis agent, which processes the data:
   - Removes duplicate results.
   - Synthesizes the information from different sources.
   - Flags any contradictions or inconsistencies.
4. **Article Writing:** 📝 The processed research results are passed to the writer agent, which generates a professional article.
5. **Real-time Streaming:** ⏳ The article is streamed back in real-time for the user to read as it is being generated.

### Example Use Case 💡:
- **Query:** "Artificial Intelligence in Healthcare" 🤖🏥
  - The user enters the query, and the app fetches the latest articles, synthesizes the research, and generates a polished article on the topic.

### Customization ⚙️:
- You can modify the models used for each agent (Web Search, Research Assistant, Writer) by changing the `MODEL` variable in the `app.py` file.
- You can also adjust the instructions for each agent (Web Search, Research Assistant, and Writer) to better suit your needs.

### Troubleshooting ⚠️:
- **Issue:** If search results aren't showing up, verify that the `duckduckgo_search` library is working correctly and returning results.
- **Issue:** If the article is not generating, ensure that your OpenAI or model API is properly configured and that the correct model is set.


