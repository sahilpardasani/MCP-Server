# MCP-Server

 This project sets up a dual-mode Model Context Protocol (MCP) server that supports both:

🧩 Tool-based responses (e.g., current time, jokes) via FastMCP
💬 Prompt-response LLM completions via FastAPI


## 📁 Project Structure

| File        | Purpose                                      |
|-------------|----------------------------------------------|
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

<img width="1787" alt="Screenshot 2025-05-27 at 1 21 35 PM" src="https://github.com/user-attachments/assets/4001416f-9a59-4507-91c1-83798c9d17c8" />
<img width="764" alt="Screenshot 2025-06-06 at 12 36 34 PM" src="https://github.com/user-attachments/assets/d1da2cbd-731e-468d-9e82-729967801d07" />

