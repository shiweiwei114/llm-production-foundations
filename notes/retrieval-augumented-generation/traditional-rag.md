Retrieval-augmented generation, or RAG, is a teachnique that uses authoriatative, external data to improve the acuuracy, relevancy, and usefulness of a model's output.

1. Ingestion: authoritative data like company proprietary data is loaded into a data source, like a Pinecone vector database
 a. Chunk the data
 b. Create vector embeddings
 c. Load data into a vector database

2. Retrieval: relevant data is retrieved from an external data source based on a user query

3. Augmentation: the retrieved data and the user query are combined into a prompt to provide the model with context for the generation step

4. Generation: the model generates output from the augmented prompt, using the context to drive a more accurate and relevant response.

