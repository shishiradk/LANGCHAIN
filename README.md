# 🦜🔗 LANGCHAIN

A concise and practical toolkit for building **language model–powered applications**, inspired by the powerful LangChain framework.

## 🔎 Overview

**LANGCHAIN** helps streamline the development of LLM-based solutions by offering modular components such as:
- Model wrappers (OpenAI, Hugging Face, etc.)
- Prompt templates with dynamic variables
- Simple chaining of prompts and LLM responses
- Built-in integrations with vector stores and memory

### Why Use LANGCHAIN?

Based on principles from LangChain—an open-source framework that empowers apps with retrieval-augmented generation, document analysis, chatbots, and more—this implementation aims to deliver a lightweight, beginner-friendly foundation for learning and prototyping.

## ⚙️ Features

- **Abstracted LLM clients**: Easy-to-use wrappers for various model providers  
- **Template-driven prompt chaining**: Pass context through a sequence of LLM calls  
- **Vector store support**: Basic integrations with popular systems  
- **Memory modules**: Persistent or session-based memory backends  
- **Ready-made examples**: Quick-start demos illustrating chains, agents, and RAG flows

## 🚀 Getting Started

### Prerequisites

- Python 3.10+  
- LLM API key (e.g., `OPENAI_API_KEY`)  
- (Optional) Vector store setup (e.g., Pinecone, Chroma)

### Install

```bash
git clone https://github.com/shishiradk/LANGCHAIN.git
cd LANGCHAIN
pip install -r requirements.txt
```

### Quick Example

```python
from langchain import OpenAI, PromptTemplate, SimpleChain

# Initialize model
llm = OpenAI(model_name="gpt-3.5-turbo")

# Define prompt template
template = PromptTemplate(
    input_vars=["topic"],
    template="Write a short story about {{topic}} in six sentences."
)

# Build chain
chain = SimpleChain(llm=llm, prompt=template)

# Run
print(chain.run({"topic": "time-traveling cat"}))
```

## 📚 Examples

Explore the `examples/` folder for more use-cases:
- **chatbot/**: Interactive conversational bot  
- **rag/**: Retrieval-augmented generation with a vector store  
- **agents/**: Simple agent implementation executing tools via LLM

## 🧩 Project Structure

```
LANGCHAIN/
├── langchain/         # Core modules: LLM, Prompts, Chains, Memory, VectorStore
├── examples/          # Demo applications and use-case scripts
├── tests/             # Unit & integration tests
├── requirements.txt   # Project dependencies
└── README.md          # This documentation
```

## ✅ Tests

Run the test suite:

```bash
pytest tests/
```

## 🛠️ Contributing

Contributions welcome! Ideas include:

- New prompt templates
- Support for additional LLM providers
- Advanced chaining logic
- Enhanced vector store integrations

Please open an issue or submit a pull request.

## 🎯 License

MIT © [Your Name or shishiradk]

---
