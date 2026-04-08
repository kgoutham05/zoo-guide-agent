# zoo-guide-agent
The zoo-agent-guide is a specific technical resource within the MCP (Model Context Protocol) Toolbox ecosystem. It is designed to help developers build and orchestrate "zoo" of specialized agents using Google's Agent Development Kit (ADK) and the MCP Toolbox.

Here is a structured summary you can copy and paste directly into your GitHub README.md.

🛠️ MCP Toolbox: Zoo Agent Guide
This project leverages the MCP Toolbox and Google's Agent Development Kit (ADK) to build a multi-agent system. The "Zoo" pattern focuses on creating a collection of specialized, modular agents that collaborate to solve complex tasks.

🌟 Key Features
Decentralized Intelligence: Instead of one massive prompt, the system uses a "Zoo" of small, specialized agents (e.g., Data Searcher, SQL Generator, Summarizer).

MCP Integration: Seamlessly connects agents to external data sources (like BigQuery, AlloyDB, or Spanner) using the Model Context Protocol.

Orchestration Patterns: Implements advanced multi-agent workflows:

Sequential: Assembly-line execution where output flows from one agent to the next.

Parallel: Simultaneous task execution for faster processing.

Loop: Iterative refinement until a specific condition is met.

Tool-First Architecture: Intelligence is shifted to the database layer via tools.yaml configurations, ensuring secure and performant data access.

<img width="1830" height="819" alt="Screenshot 2026-04-08 235348" src="https://github.com/user-attachments/assets/4ca526d8-eb6a-4db0-8058-b4c8a4de03fe" />


🚀 Getting Started
1. Environment Setup
Ensure you are working in a Python virtual environment and have the ADK installed:

Bash
python3 -m venv .venv
source .venv/bin/activate
pip install toolbox-adk
2. Running the Agent UI
To interact with your "Zoo" of agents via a browser-based interface:

Bash
adk web --port 8000
Note: If port 8000 is in use, use fuser -k 8000/tcp to clear it.

3. Defining Tools
Tools are defined in the tools.yaml file, allowing your agents to interact with BigQuery or other Google Cloud services without writing complex boilerplate code.

📂 Project Structure
my-agents/: Contains individual agent definitions and logic.

tools.yaml: Configuration for MCP tool sources (e.g., BigQuery, Cloud SQL).

.adk/: Local storage for agent artifacts and session memory.

💡 Why use this guide?
The Zoo Agent Guide addresses the "Production Readiness Barrier" by providing a vetted implementation pattern. It moves beyond simple "toy" examples into scalable, enterprise-ready agentic architectures that are secure enough for real-world database interactions.
