# Chainlit

## Setup
1. Clone the repo 

2. Make sure you have `uv` installed,

3. Install the necessary packages, it also creats the virtual environment for you.
    ```
    uv sync
    ```

4. We will use Qdrant locally, so lets provide qdrant url in the `.env` file.
    ```
    docker pull qdrant/qdrant
    docker run -p 6333:6333 -p 6334:6334 \
    -v $(pwd)/qdrant_storage:/qdrant/storage:z \
    qdrant/qdrant
    
4. Run the chainlit app
    ```
    uv run ingest.py
    uv run chainlit run rag-chainlit-deepseek.py
    ```