# Tamil Nadu Agriculture Schemes Knowledge Graph Chatbot

A chatbot that answers questions about Tamil Nadu government agriculture schemes by querying a Neo4j knowledge graph built from scheme pages.

> Part of my Gen AI course practice work (Week 3, Day 1).

## Tech stack

- Python 3
- Neo4j
- LangChain (`GraphCypherQAChain`)
- OpenAI
- Streamlit

## Features

- `ingest.py` scrapes scheme pages from tn.gov.in and loads them into Neo4j
- `app.py` Streamlit chat UI that turns questions into Cypher queries
- English and Tamil answers (language switch in the sidebar)

## Getting started

1. Clone the repository:
   ```bash
   git clone https://github.com/Prembazskar/knowledge-graph-rag-neo4j-chatbot.git
   cd knowledge-graph-rag-neo4j-chatbot
   ```
2. Install and configure:
   ```bash
   pip install -r requirements.txt
   cp .env.example .env   # OpenAI key and Neo4j connection details
   ```

Environment variables (set in `.env`, never commit it):

- `OPENAI_API_KEY`
- `NEO4J_URI`
- `NEO4J_USERNAME`
- `NEO4J_PASSWORD`
- `NEO4J_DATABASE`

## Usage

```bash
python ingest.py        # build the graph once
streamlit run app.py
```

## License

MIT, see [LICENSE](LICENSE).
