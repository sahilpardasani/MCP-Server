# MCP-Server

 This project sets up a dual-mode Model Context Protocol (MCP) server that supports both:

🧩 Tool-based responses (e.g., current time, jokes) via FastMCP
💬 Prompt-response LLM completions via FastAPI


## 📁 Project Structure

| File        | Purpose                                      |
|-------------|----------------------------------------------|
| `app.py`    | FastAPI entrypoint and route `/generate`     |
| `server.py` | Handles LLM loading, generation, config      |


🚀 Features

⚙️ Compatible with Claude Desktop, MCP Inspector, LangGraph, etc.
🔌 FastMCP standard for tool registration and stdin communication
🧠 Run local LLM completions from app.py using /generate API
🌐 Optional HTTP server mode for broader integrations
🧪 MCP tools return structured JSON responses

🛠 Installation
pip install fastapi uvicorn transformers torch
pip install requests
pip install bitsandbytes accelerate  # Only needed if using quantized models

🛠 Registered MCP Tools
Tool Name	  What It Does
time_now	  Returns current UTC timestamp
dad_joke	  Returns a random dad joke from API

💡 What is MCP?
Model Context Protocol (MCP) allows custom tools and local models to be integrated into AI assistants like Claude Desktop or LangGraph. You can register Python functions as tools, and they become callable by the assistant when relevant.
