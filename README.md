# BlockchainGraphToVector-RAG
Data processing and analysis pipeline designed for the blockchain logs. This project involves querying the Sui blockchain using GraphQL, processing logs from a graph database, embedding the data using OpenAI, and storing and querying the data in a Weaviate vector database for retrieval-augmented generation (RAG).

## Description

SuiBlockchainRAGPipeline is a comprehensive data processing and analysis pipeline designed for the Sui blockchain. This project involves querying the Sui blockchain using GraphQL, processing logs from a graph database, embedding the data using OpenAI, and storing and querying the data in a Weaviate vector database for retrieval-augmented generation (RAG). The pipeline leverages advanced techniques to analyze variable and highly nested JSON logs, enabling insightful metrics and queries using a language model.

## Key Components

- **Sui Blockchain GraphQL**: Fetch transaction data and metadata from the Sui blockchain using GraphQL queries.
- **Graph Database**: Process and store transaction logs in a graph database for efficient querying and analysis.
- **OpenAI for Embedding**: Use OpenAI models to embed and transform the data for enhanced analysis and insights.
- **Weaviate for RAG**: Store the embedded data in Weaviate, a powerful vector database, and utilize retrieval-augmented generation (RAG) techniques for advanced querying and metrics building.

## Workflow

1. **get_digests.ipynb**:
   - Query the Sui blockchain using GraphQL to fetch transaction digests.
   - Save the retrieved digests to a JSON file.

2. **get_raw_json.ipynb**:
   - Load the transaction digests from the JSON file.
   - Query the Sui blockchain to fetch detailed metadata for each transaction digest.
   - Save the detailed metadata to a JSON file.

3. **weaviate_load.ipynb**:
   - Load the transaction metadata from the JSON file.
   - Embed the data using OpenAI models.
   - Store the embedded data in a Weaviate vector database.
   - Perform advanced queries and generate metrics using retrieval-augmented generation (RAG) techniques.

## Dependencies

- Python 3.x
- Jupyter Notebook
- Pandas
- gql
- asyncio
- Weaviate Python Client
## Running the Workflow

1. **Fetch Transaction Digests:**
   Open and run `get_digests.ipynb` in Jupyter Notebook to fetch transaction digests and save them to `digests.json`.

2. **Retrieve Transaction Metadata:**
   Open and run `get_raw_json.ipynb` in Jupyter Notebook to retrieve detailed transaction metadata and save it to `digest_metadata.json`.

3. **Load Data into Weaviate and use LLM to analyze logs:**
   Open and run `weaviate_load.ipynb` in Jupyter Notebook to load the metadata into Weaviate, embed the data, and perform advanced queries.
