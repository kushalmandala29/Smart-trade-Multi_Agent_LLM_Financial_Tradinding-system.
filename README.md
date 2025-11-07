# Smart-trade: Multi-Agent LLM Trading System

Short description  
A research-oriented, modular multi-agent trading framework that composes specialized LLM-powered agents (analysts, researchers, traders, and risk managers) to generate market insights and simulated trading decisions.

Quick links
- Usage: see the Usage section below
- Configuration: check tradingagents/default_config.py
- Workflow diagram: see the Workflow diagram section below
- License: MIT (or your selected license)

Table of contents
- Installation
- Configuration / API keys
- Usage (CLI and Python)
- Workflow diagram
- Project structure
- Contributing
- License
- Contact

Installation
1. Clone your fork:
   ```bash
   git clone https://github.com/kushalmandala29/Smart-trade-Multi_Agent_LLM_Financial_Tradinding-system.
   cd Smart-trade-Multi_Agent_LLM_Financial_Tradinding-system.
   ```
2. Create a Python environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # macOS / Linux
   .\.venv\Scripts\activate   # Windows
   ```
3. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```

Configuration / API keys
This project may use third-party APIs for market and LLM access. Set environment variables:
```bash
export FINNHUB_API_KEY="<your_finnhub_api_key>"
export OPENAI_API_KEY="<your_openai_api_key>"
```
(Adapt to your preferred provider and local OS.)

Usage

CLI  
Run the command-line interface to interactively run agents:
```bash
python -m cli.main
```

Python API  
Example usage inside Python:
```python
from tradingagents.graph.trading_graph import TradingAgentsGraph
from tradingagents.default_config import DEFAULT_CONFIG

ta = TradingAgentsGraph(debug=True, config=DEFAULT_CONFIG.copy())
_, decision = ta.propagate("NVDA", "2024-05-10")
print(decision)
```

Workflow diagram
The following Mermaid diagram captures the end-to-end orchestration of inputs, analyst and researcher agents, trading, risk, execution, and metrics.

<img width="4753" height="2154" alt="mermaid-ai-diagram-2025-11-07-114822" src="https://github.com/user-attachments/assets/2b9e6414-c165-4deb-9658-0414321aa10b" />


Project structure (high-level)
- tradingagents/         — package implementing agent graphs and tools
- cli/                   — command-line application
- assets/                — images and example assets (may contain references to upstream; consider replacing)
- docs/                  — documentation and examples (if present)
- requirements.txt       — Python dependencies

Contributing
Contributions are welcome. If you want to:
- Fix bugs, improve docs, or add features: open a PR on this fork.
- Prefered workflow: fork → feature branch → PR.

License
Specify your license here (e.g., MIT). If no LICENSE file exists in the repo, I can add one for you.

Contact
Maintainer: kushalmandala29  
Repository: https://github.com/kushalmandala29/Smart-trade-Multi_Agent_LLM_Financial_Tradinding-system.
