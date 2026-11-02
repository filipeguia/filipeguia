# Filipe Guia

AI automation engineer and quantitative researcher. I work solo from Brazil (UTC-4), on a single laptop with an 8 GB GPU, and I am open to remote contract work with US time zone overlap

I build LLM systems with fixed output formats, validation, spending limits and human approval steps, with tests that run without network access. In research I write the test and the pass criteria before running it, and I reimplement anything that passes before I trust it

- Python since 2016, LLMs since late 2022, AI coding agents every day since May 2025: over 57 billion tokens on OpenAI alone as of November 2026, with a peak of 4.9 billion in one day running several agents in parallel. Most of that volume is cached context, since agents reread the codebase at every step
- Research that transfers about 5 TB of market data a month
- Founder of Survey Horizon, a surveying company, so I am used to serving paying clients and meeting deadlines

## Featured work

### Customer messaging pipeline
Private, built for my own company

Answers customers on WhatsApp and prepares proposals without anything going out unchecked. A first agent sorted incoming contacts (client or not, type of request) and answered from the service portfolio. Requests went to a second agent that drafted proposals from past contracts (language, pricing, method), and the internal team approved every proposal before it was sent. For client work I build this on the official WhatsApp Business Platform

### LLM Ensemble Trader Lab
Public repository: [llm-ensemble-trader-lab](https://github.com/filipeguia/llm-ensemble-trader-lab)

Shows how to keep an LLM inside a decision loop under control. Several agents answer each market event with a structured trading decision, and only valid answers count toward a quorum vote. The run is priced before it starts and stops at a spending cap. It runs offline with a mock, through the Anthropic API, or by exchanging files with agent CLIs, and 216 tests run without network access. The trading policy is a toy example, with no profit claims

### Invoice extraction lab
Coming soon

Turns invoice PDFs into checked data and sends doubtful cases to a person. Business rules check line items, subtotal, tax, totals and dates, the model gets a second try with its own errors, and low-confidence invoices go to human review. The test set has 60 synthetic invoices with known answers: 24 in 6 layouts the hand-written rules were built for, 28 in 7 layouts they never saw, and 8 scans with no text layer. Counting a field as correct only when it matches the answer after normalizing dates and amounts, the rules get 98.7% of fields right on the known layouts, 62.5% on the unseen ones and cannot read the scans. The LLM results are being measured now

## More builds

- **Browser control for coding agents** (prototype in daily use): built in April 2026, when the computer-use tools available were not reliable enough to run my agents on logged-in web apps. It went from a screenshot loop driving a vision model to a Chrome extension with a local REST service, page snapshots with element references and per-agent tab locks, so several agents work in parallel
- **Custom cloud drive for Windows** (in daily use): built when the OneDrive desktop client kept freezing. A C++ provider on the Windows Cloud Files API shows several cloud accounts and physical disks as one folder in Explorer, downloads files on demand and frees local space only after the upload is confirmed
- **Unreal Engine MCP server and image to 3D** (in use in my own projects): an MCP server with 66 tools and no third-party dependencies drives Unreal Engine 5 through a C++ bridge. Reference images become detailed 3D models with Hunyuan3D, TRELLIS and TripoSR running locally on the 8 GB GPU (Meshy as a hosted comparison), and the server brings them into the scene
- **Trading operations bot:** MetaTrader 5 expert advisors report to Telegram, and trades can be checked and controlled from there
- **Legacy software modernization:** rebuilt my own copies of Windows programs more than 20 years old that had no source code, by reverse engineering their behavior and file formats and reimplementing them with AI coding agents. For clients, I do this only on software they own or are licensed to modify
- **Geospatial automation** (client work at my company): drone photogrammetry in Agisoft Metashape automated with Python, GNSS processing and CAD drawing generation. Also the analysis behind a 600 km highway concession bid, with 997 rural properties and 12,770 land parcels checked against the corridor and the proposal delivered in 5 days

## Research discipline

- **Research memory for agents:** about 1,200 notes in Obsidian where agents record what was tested, how, and why it was kept or dropped, to reduce repeated testing of rejected ideas
- **What gets rejected:** more than 180 strategy families built on external data were tested and rejected, including neural decision models in PyTorch and genetic search over neural networks inside walk-forward tests
- **A validation bug I caught:** a candidate that had passed was entering 2 to 3 hours before its own signal, because the backtester compared server time with UTC timestamps. An independent reimplementation found it, and the candidate was dropped
- **Speed:** backtest engines in Numba and CUDA, checked trade by trade against the MetaTrader 5 Strategy Tester

## How I work

I write the spec and the acceptance tests first, AI coding agents do much of the implementation, and I own the architecture and the code review. I check a platform's terms and use its official integrations before automating it, and I do not sell trading signals or promise returns

## Contact

Tell me which process you want to automate, or which research question you want tested, and I will reply with a short plan

filipestateofart@gmail.com
