AI Voice Assistant
An AI assistant built with n8n, Qdrant, Groq, Gemini, and Tavily.
It supports web search, knowledge base search, and hybrid answers using both uploaded documents and live web results.

Features
Chat-based assistant UI
PDF upload to knowledge base
Qdrant vector search
Web search using Tavily
AI router for choosing:
Web search
Knowledge base
Hybrid mode
Text output + browser speech output
n8n automation workflows
Tech Stack
n8n
Qdrant
Groq Llama
Gemini Embeddings
Tavily Search API
HTML, CSS, JavaScript
Project Structure
AI-Voice-Assistant/
├── index.html
├── README.md
├── .gitignore
└── Workflows/
    ├── ask-query.json
    └── upload-kb.json


## Setup

### 1. Clone the repository

```bash
git clone https://github.com/sanyaa06/AI-Voice-Assistant.git
cd AI-Voice-Assistant
2. Import the n8n workflows
Import the following workflow files into your n8n instance:

Workflows/ask-query.json
Workflows/upload-kb.json
3. Configure API keys
Replace the placeholder values in the workflows (or configure them through n8n credentials) with your own:

Groq API Key
Tavily API Key
Google Gemini API Key
Qdrant API Key
4. Set up Qdrant
Create a Qdrant Cloud cluster.
Create a collection named kb_base.
Update the Qdrant endpoint and API key in the workflow.
5. Publish the workflows
Publish both workflows in n8n and copy their production webhook URLs.

Example:

https://your-instance.app.n8n.cloud/webhook/voice-agent
https://your-instance.app.n8n.cloud/webhook/upload-kb
6. Configure the frontend
Update the webhook URLs in index.html:

const assistantWebhook = "YOUR_PRODUCTION_WEBHOOK_URL";
const uploadWebhook = "YOUR_UPLOAD_WEBHOOK_URL";
7. Run the application
Open index.html in your browser.

You can now:

💬 Ask questions through the AI assistant
📄 Upload PDF documents to your knowledge base
🔍 Get answers from:
Web Search
Knowledge Base
Hybrid (Knowledge Base + Web Search)
