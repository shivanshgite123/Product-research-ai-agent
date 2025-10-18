# Patent Innovation Predictor 🔬

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

A powerful agentic AI system for patent trend analysis and future technology prediction using Ollama, OpenSearch, and CrewAI.

## 🚀 Features

- 🤖 Multi-agent system with specialized roles
- 🔍 Advanced patent data analysis
- 📊 Technology trend identification
- 🔮 Future innovation prediction
- 🔄 Iterative search refinement
- 📈 Real-time data processing

## 📖 Overview

This system leverages artificial intelligence to analyze patent data and predict future technological innovations, with a special focus on lithium battery technology. It employs a sophisticated multi-agent architecture featuring specialized roles:

- Research Director
- Patent Retriever
- Data Analyst
- Innovation Forecaster

## 🏗️ System Architecture

```
┌───────────────────────────────────────────────────────────────┐
│                     User Interface Layer                      │
└───────────────────────────────────────────────────────────────┘
                │                │                │
                ▼                ▼                ▼
┌───────────────────────────────────────────────────────────────┐
│                 Agent Orchestration Layer                     │
│  ┌──────────────────┐   ┌────────────────┐  ┌───────────────┐│
│  │ Research Director│   │Patent Retriever│  │Data Analyst   ││
│  └──────────────────┘   └────────────────┘  └───────────────┘│
│                                                               │
│  ┌──────────────────┐                                         │
│  │Innovation        │                                         │
│  │Forecaster        │                                         │
│  └──────────────────┘                                         │
└───────────────────────────────────────────────────────────────┘
```

## 🔧 Prerequisites

- Python 3.10+
- Docker & Docker Compose
- Ollama
- OpenSearch
- Patent dataset (pre-loaded in OpenSearch)

## 📥 Installation

1. **Clone the repository**
```powershell
git clone https://github.com/yourusername/patent-innovation-predictor.git
cd patent-innovation-predictor
```

2. **Set up Python environment**
```powershell
python -m venv .venv
.\.venv\Scripts\activate  # Windows
```

3. **Install dependencies**
```powershell
pip install -r requirements.txt
```

4. **Start Ollama container**
```powershell
docker run -d -v ollama:/root/.ollama -p 11434:11434 --name ollama ollama/ollama
```

5. **Pull required models**
```powershell
docker exec -it ollama ollama run deepseek-r1:1.5b
docker exec -it ollama ollama run nomic-embed-text
```

6. **Launch OpenSearch**
```powershell
docker compose up -d
```

## ⚙️ Configuration

### Environment Setup
Create a `.env` file in the project root:
```env
SERPAPI_API_KEY=your_key_here
OPENSEARCH_HOST=localhost
OPENSEARCH_PORT=9200
```

### OpenSearch Setup
The system automatically creates required indices on first run.

## 🚀 Usage

1. **Start the application**
```powershell
python agentic_rag.py
```

2. **Access the interface**
Navigate to `http://localhost:8000` in your browser

## 🤝 Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

