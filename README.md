# SaaS Price & Review Agent 💼💬

A dual-agent chatbot system that helps users make informed decisions about SaaS products — by offering **customized pricing predictions** and **AI-powered review comparisons**.

---

## 🧠 About the Project

This project consists of two key components: a **Pricing Agent** and a **Review Agent**, both designed to streamline SaaS product evaluation.

### 💸 Pricing Agent

The **Pricing Agent** is a chatbot-style tool built using **OpenAI’s Function Calling** feature. It provides tailored pricing information for SaaS products based on:

- Customized **workload count**
- Company **tier** (Startup, SME, or Enterprise)

#### How it works:
- Prices of various SaaS products were scraped directly from their official websites.
- A standard **15% discount margin** was applied across all products.
- These normalized prices were stored in a structured `JSON` file.
- Using OpenAI's function calling, the chatbot:
  - Understands user queries
  - Retrieves the appropriate price from the database
  - Responds with a customized price based on user input

The main goal was to build a dynamic pricing assistant that delivers **context-aware**, **real-time** responses to user queries.

---

### 📝 Review Agent

The **Review Agent** is a chatbot powered by **Retrieval-Augmented Generation (RAG)** that allows users to:

- Fetch relevant SaaS product reviews
- Compare competing products
- Explore user migration trends between tools

#### How it works:
- Reviews were scraped from trusted platforms like **G2**, **Quora**, and **Reddit**
- These reviews were:
  - Preprocessed and split into chunks
  - Stored in a **ChromaDB vector store**
- A **LangChain-based RAG pipeline** was built to:
  - Perform semantic search on user queries
  - Fetch matching review chunks
  - Return insightful, conversational responses

#### 🔁 Migration Analysis
A dedicated feature highlights user migration trends:
- For each SaaS product, key competitors are listed
- Users can view **where people are switching to and why**
- This helps users make better-informed decisions based on trends and peer feedback

---

## ⚙️ Tech Stack

- Python
- OpenAI GPT (with Function Calling)
- LangChain
- ChromaDB (Vector Database)
- BeautifulSoup / Scrapy (for scraping)
- JSON (for price storage)
