# AI-Powered T-Shirt Store Inventory Assistant 👕

An end-to-end LLM-based application that enables natural language interaction with a MySQL database. This system allows users to query inventory, sales, and discount data using plain English, which is then converted into optimized SQL queries for real-time execution.

## 🚀 Project Overview

Managing retail inventory often involves complex SQL queries that can be a barrier for non-technical users. This project bridges that gap by providing a conversational interface for a T-shirt store database. 

**Example Queries:**
* *"How many white Adidas T-shirts are left in stock?"*
* *"What is the projected revenue if we sell all extra-small Nike shirts after applying current discounts?"*

## ✨ Key Features

- **Natural Language to SQL:** Seamlessly converts user questions into executable SQL using Google Gemini.
- **Few-Shot Learning:** Leverages **ChromaDB** as a vector store to retrieve relevant query examples, significantly improving the model's accuracy for complex joins and logic.
- **Dynamic Discount Handling:** Automatically calculates potential revenue by joining inventory data with active discount tables.
- **Interactive UI:** A clean, responsive dashboard built with **Streamlit** for real-time data visualization.

## 🛠️ Tech Stack

- **LLM:** Google Gemini
- **Framework:** LangChain
- **Database:** MySQL
- **Vector Store:** ChromaDB (for Few-Shot Prompting)
- **Embeddings:** Hugging Face
- **Frontend:** Streamlit
- **Language:** Python

## 🏗️ System Architecture

1. **User Query:** User enters a natural language question.
2. **Semantic Search:** The system searches ChromaDB for the most similar "Question-SQL" pairs to provide context to the LLM.
3. **Query Generation:** The LLM generates a syntactically correct SQL query based on the schema and few-shot examples.
4. **Execution:** The query runs against the MySQL database.
5. **Response:** The results are formatted into a natural language answer for the user.

## ⚙️ Installation

1. **Clone the Repository:**
   ```bash
   git clone [https://github.comvedakshari1-collab/T-shirts-selling-store.git](https://github.com/vedakshari1-collab/T-shirts-selling-store.git)
   cd T-shirts-selling-store
**Sample Questions**
*"How many total T-shirts are left in stock?"*
*"Show me the inventory for Nike XS white shirts."*
*"What is the total value of the inventory for all 'Small' size T-shirts?"*
*"Calculate the total revenue for Adidas shirts after applying active discounts."*
