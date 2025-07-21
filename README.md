---------------------------------------------------------------------------------
|                                                                               |
|  Raw Logs / Events (Unstructured Text)                                        |
|        ↓                                                                      |
|  Log Preprocessing (Cleaning & Normalizing)                                   |
|        ↓                                                                      |
|  Log Embedding (Sentence-BERT / LogBERT Model)                               |
|        ↓                                                                      |
|  Clustering & Outlier Detection (HDBSCAN/DBSCAN)                             |
|        ↓                                                                      |
|  Vector Store for Threat Intel & Historical Context (FAISS / Pinecone)        |
|        ↓                                                                      |
|  Retrieval Component (Nearest Neighbor Search)                               |
|        ↓                                                                      |
|  LLM Generation (GPT / LLaMA + Retrieved Context)                            |
|        ↓                                                                      |
|  Analyst Dashboard (Visualize & Take Action)                                 |
