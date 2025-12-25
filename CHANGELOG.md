# Changelog


- Initial release of **RAG QA Logs & Corpus — Multi-Table Synthetic RAG Benchmark**.
- Added **6 linked CSV tables**:
  - Document corpus (`rag_corpus_documents.csv`)
  - Chunk index (`rag_corpus_chunks.csv`)
  - Retrieval events (`rag_retrieval_events.csv`)
  - QA evaluation runs (`eval_runs.csv`)
  - Scenario templates (`scenarios.csv`)
  - Data dictionary (`data_dictionary.csv`)
- Included core supervision targets:
  - `is_correct`, `hallucination_flag`, `faithfulness_label`
- Included key RAG telemetry:
  - retrieval metrics (rank/score/relevance + recall/mrr signals)
  - latency (`latency_ms_retrieval`, `latency_ms_generation`, `total_latency_ms`)
  - token usage (`prompt_tokens`, `answer_tokens`)
  - approximate cost (`total_cost_usd`)
- Stable join keys across tables:
  - `doc_id`, `chunk_id`, `example_id`, `run_id`, `scenario_id`, `query_id`
- Privacy note:
  - all records are **fully synthetic** (no real users/customers/company data).
