LLM-Powered Chat-to-Database Assistant for FX-Tees

### 🔍 Project Overview

This is an **end-to-end LLM project** built for **FX-Tees**, a fictional T-shirt store. The objective is to empower non-technical users to interact with a MySQL database using **natural language**. Users can ask questions like *"How many white Nike T-shirts are in stock?"* and receive accurate responses — powered by **Google PaLM LLM**, **LangChain**, and **SQL query generation**.

### 🛠️ Tech Stack

* **LLM**: Google PaLM (via LangChain)
* **Embedding & Retrieval**: HuggingFace + ChromaDB
* **Frontend UI**: Streamlit
* **Database**: MySQL (with `tshirts` and `discounts` tables)
* **Backend Logic**: LangChain’s SQLDatabaseChain for query translation and execution

---

### 🧰 Key Features & Use Case

1. **Natural Language to SQL**:
   Converts user questions into SQL queries using Google PaLM LLM and executes them directly on a structured MySQL database.

2. **Embeddings for Complex Queries**:
   For queries where the LLM struggles, a few-shot prompt strategy with sentence embeddings (via HuggingFace) and ChromaDB ensures better accuracy and context awareness.

3. **No-Code UI**:
   A lightweight **Streamlit app** enables business users (non-technical staff) to ask ad-hoc questions and view answers instantly — without needing SQL knowledge or Excel workarounds.

---

### 🧱 Database Schema (Simplified)

* `tshirts` table: stores brand, color, size, price per unit, and inventory quantity
* `discounts` table: maps `tshirt_id` to current discount %

---

### 🚀 Workflow Steps

1. **User enters a question** (e.g., *"How many black Adidas t-shirts are in stock?"*)
2. **LangChain's SQLDatabaseChain** uses Google PaLM to generate a SQL query.
3. **Query is executed** on the MySQL database and results are shown to the user.
4. For **complex queries**, training examples are embedded and stored in **ChromaDB** for semantic retrieval to assist the LLM.
5. **Streamlit UI** ties it all together, providing a friendly frontend interface.

---

### 🎯 Real-World Use Case

This tool can significantly reduce dependency on analysts for ad-hoc queries in **retail, inventory management, and reporting** scenarios. It makes data access conversational, democratizing insights for all team members.
