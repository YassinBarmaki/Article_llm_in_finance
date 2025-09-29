# Article_llm_in_finance
Bilingual, Cross-Market Financial Analytics via Retrieval-Augmented Generation: Evidence Traceability and Factuality at Scale. 
Authors   
Mohammad Yasin Barmaki, Master of Information Technology Management, University of Tehran, Iran     Email: yassin.barmaki@ut.ac.ir 
Dr. Babak Sohrabi, Full Professor of Information Technology Management, University of Tehran, Iran    Email: bsouhrabi@ut.ac.ir

Abstract
We present a bilingual, retrieval-grounded framework for stock-market analysis across the Tehran Stock Exchange (TSE) and the New York Stock Exchange (NYSE).
The system couples instruction-tuned GPT-4 with prompt guardrails to a Retrieval-Augmented Generation (RAG) pipeline over a FAISS index built from time-walled
disclosures (SEC, TSETMC) and market data (Yahoo Finance). At query time, the model follows a retrieve → ground → generate → score pattern: top-k evidence is
fetched and cited by ID and timestamp; the answer is then complemented with classical forecasts (ARIMA for trend; GARCH for volatility), technical indicators
(RSI, MACD), and multilingual sentiment (FinBERT for English; ParsBERT for Persian). We introduce Fact-Score+, a sentence-level factuality measure combining
token-overlap with embedding similarity. On held-out queries, the framework attains 89.5% (TSE) and 92.5% (NYSE) factual alignment, and the Full system
outperforms ablations (No-RAG, No-Forecast, No-Sentiment) on both linguistic and factuality metrics. Forecasting modules reduce error relative to language-only
baselines (MAPE for TSE; RMSE for NYSE) while remaining interpretable and fast. The entire pipeline runs on commodity resources (Google Colab Pro and paid API
access), writes run manifests and evidence logs for audit, and exposes configuration via environment variables (e.g., FAISS_PATH=./data/faiss_dual_market).
By combining grounded generation, transparent retrieval, and lightweight quantitative modeling, the framework delivers bilingual, cross-market analyses that are
accurate, auditable, and reproducible offering a practical foundation for trustworthy financial AI in both emerging and developed markets.

Keywords: Large language models (LLMs); Generative AI; Retrieval-Augmented Generation; FAISS; bilingual NLP; financial forecasting; ARIMA; GARCH; FinBERT;
ParsBERT; Fact-Score+; Tehran Stock Exchange (TSE); New York Stock Exchange (NYSE).
