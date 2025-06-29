# DiabetesGraphRAG

Welcome to my **DiabetesGraphRAG** project! This Google Colab notebook (`GraphRag_with_Neo4j.ipynb`) builds a knowledge graph about diabetes using Neo4j and an AI language model. It pulls medical info from Wikipedia, creates a graph of relationships, and answers questions about diabetes. Perfect for learning about knowledge graphs, AI, and medical data!

## 📖 What’s This Project?

This notebook creates a system to:
- Fetch diabetes info from Wikipedia.
- Build a knowledge graph in Neo4j to store relationships.
- Answer questions like “What are the symptoms of Type 2 diabetes?” using graph and text data.
- Visualize the graph interactively.

It’s a fun way to explore combining AI, graphs, and medical knowledge!

## ✨ Features
- Extracts medical entities (diseases, symptoms, treatments) using AI.
- Stores and queries data in a Neo4j graph database.
- Answers natural language questions about diabetes.
- Visualizes the knowledge graph in the notebook.
- Combines graph-based and text-based search for better answers.

## 🛠 What You’ll Need
- A **Neo4j Aura** account (free tier) or local Neo4j setup.
- A **Grok API key** from [xAI](https://x.ai/api) (or another model like HuggingFace).
- [Google Colab](https://colab.research.google.com/) or a local Jupyter Notebook.
- Basic Python skills.

## 🚀 Setup Steps
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/<your-username>/<your-repo-name>.git
   cd <your-repo-name>
   ```

2. **Set Up Neo4j**:
   - Create a free [Neo4j Aura](https://neo4j.com/cloud/aura/) account or install Neo4j locally.
   - Add your Neo4j credentials in the notebook:
     ```python
     NEO4J_URI = "neo4j+s://<your-instance>.databases.neo4j.io"
     NEO4J_USERNAME = "neo4j"
     NEO4J_PASSWORD = "<your-password>"
     ```

3. **Add Your API Key**:
   - Get a Grok API key from [xAI](https://x.ai/api).
   - In Google Colab, store it securely:
     ```python
     from google.colab import userdata
     GROQ_API_KEY = userdata.get('GROQ_API_KEY')
     os.environ["GROQ_API_KEY"] = GROQ_API_KEY
     ```

4. **Install Dependencies**:
   Run these commands in the notebook:
   ```bash
   !pip install --upgrade --quiet langchain langchain-community langchain-openai langchain-experimental neo4j wikipedia tiktoken
   !pip install wikipedia
   !pip install langchain-groq
   !pip install yfiles_jupyter_graphs
   !pip install neo4j pyvis
   !pip install langchain-huggingface
   !pip install -U langchain-neo4j
   ```

5. **Run the Notebook**:
   - Open `GraphRag_with_Neo4j.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter.
   - Run cells in order to load data, build the graph, and test it.

## 🎮 How to Use It
- **Load Data**: Pulls diabetes info from Wikipedia and splits it into chunks.
- **Build the Graph**: Extracts entities and relationships, storing them in Neo4j.
- **Ask Questions**: Try questions like:
  - “What are the types of diabetes?”
  - “How is Type 1 diabetes managed?”
  - “Can obesity cause Type 2 diabetes?”
- **Visualize**: Use `showGraph()` to see the knowledge graph.
- **Get Answers**: Combines graph and text data for clear answers.

## 📦 Libraries Used
- `langchain`, `langchain-community`, `langchain-groq`, `langchain-huggingface`, `langchain-neo4j`
- `neo4j` (graph database)
- `wikipedia` (data source)
- `yfiles_jupyter_graphs` (visualization)
- `sentence-transformers` (embeddings)
- `tiktoken`, `pyvis`

## ❓ Example Questions
- What are the symptoms of Type 2 diabetes?
- How does Type 1 diabetes differ from Type 2?
- What lifestyle changes reduce diabetes risk?

## 🙌 Contributing
I’m a software engineering student, and this is a learning project! Want to help?
- Fork the repo.
- Create a branch: `git checkout -b my-cool-feature`
- Commit changes: `git commit -m "Added something awesome"`
- Push: `git push origin my-cool-feature`
- Open a Pull Request.

Suggestions and feedback are super welcome!

## 📌 Note
This notebook is designed to run in Google Colab for ease of use. If you run it locally, ensure all dependencies are installed in your Python environment.
