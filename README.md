# Multi-Agent Research System

This project implements a **multi-agent pipeline** for automated literature review and research synthesis.  
It uses specialized agents and external tools to fetch, parse, read, write, and critique research outputs.

---

## 🚀 Workflow Overview

1. **Research Topic Input**  
   - User provides a research topic (e.g., *"Impact of AI on Healthcare"*).

2. **Search Agent**  
   - Fetches initial results related to the topic.  
   - Results are passed to **Tool 1: Tavily API** for live web search.  
   - Tavily returns enriched search results which are **saved**.

3. **Reader Agent**  
   - Consumes saved Tavily results.  
   - Passes them to **Tool 2: BeautifulSoup Scraper** for parsing and content extraction.  
   - Parsed data is returned to the Reader Agent and **saved**.

4. **Writer Agent**  
   - Takes the Reader Agent’s processed results.  
   - Synthesizes a structured research draft (summary, insights, references).

5. **Critic Agent**  
   - Reviews the Writer Agent’s draft.  
   - Provides feedback, corrections, and ensures clarity, accuracy, and coherence.  
   - Produces the **final polished output**.

---

## 🛠️ Tools Used

- **Tavily API** → Live web search results for up-to-date information.  
- **BeautifulSoup** → HTML parsing and content extraction from web pages.

---

## 📂 Project Structure
  multi-agent-research-system/
│
├── agents/
│   ├── search_agent.py      # Handles topic search + Tavily API
│   ├── reader_agent.py      # Reads + parses results with BeautifulSoup
│   ├── writer_agent.py      # Synthesizes structured draft
│   └── critic_agent.py      # Reviews and critiques draft
│
├── tools/
│   ├── tavily_api.py        # Wrapper for Tavily API calls
│   └── bs_parser.py         # BeautifulSoup parser utility
│
├── main.py                  # Orchestration pipeline
├── README.md                # Documentation (this file)
└── requirements.txt         # Dependencies


---

## ⚙️ Installation

git clone https://github.com/your-username/multi-agent-research-system.git
cd multi-agent-research-system
pip install -r requirements.txt

## Usage
python main.py "Impact of AI on Healthcare"

Topic: "Impact of AI on Healthcare"

Search Agent → Tavily API → Results saved
Reader Agent → BeautifulSoup → Parsed content saved
Writer Agent → Draft synthesis
Critic Agent → Final polished output


## Installation
pip install -r requirements.txt




