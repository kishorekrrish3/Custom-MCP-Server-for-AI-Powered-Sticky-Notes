# 🧠 Custom MCP Server for AI-Powered Sticky Notes

A lightweight, customizable MCP (Multi-Command Protocol) server for managing sticky notes using natural language commands — ideal for productivity, reminders, and AI-enhanced ideation. Built with [FastMCP](https://github.com/ai-collection/mcp), and powered by the blazing-fast [uv](https://github.com/astral-sh/uv) package manager.

---

## 🚀 Features

- ✅ Built with a **Custom MCP Server**
- 📝 Supports **adding, reading, and retrieving** sticky notes
- 📁 Notes are persistently stored in a local `.txt` file
- ⚙️ Easily integrates with the **Claude Desktop App**
- ⚡ Powered by `uv` for fast and modern Python project management

---

## 💪 Setup & Installation

### 1. Install `uv`

#### For **Windows** (PowerShell):
```powershell
powershell -ExecutionPolicy ByPass -c "irm https://astral.sh/uv/install.ps1 | iex"
```

#### For **Mac/Linux** (with `curl`):
```bash
curl -LsSf https://astral.sh/uv/install.sh | sh
```

#### Or with `wget`:
```bash
wget -qO- https://astral.sh/uv/install.sh | sh
```

> 💡 You can also install a specific version:  
> `curl -LsSf https://astral.sh/uv/0.6.14/install.sh | sh`

---

### 2. Initialize Project
```bash
uv init .
```

---

### 3. Add MCP as a dependency
```bash
uv add "mcp[cli]"
```

---

## 🔄 Run the MCP Server

Place all your server logic inside a `main.py` file (as shown in this repo).

Then, install the MCP with:
```bash
uv run mcp install main.py
```

This registers your custom MCP server with compatible clients.

---

## 🚧 Claude Desktop Integration

If you have the **Claude desktop app** installed:

- Simply run:
  ```bash
  uv run mcp install main.py
  ```
- Claude will auto-detect and register your custom MCP server.
- If you don’t see the new tools or commands:
  1. End task the Claude app from Task Manager
  2. Restart the Claude Desktop app
  3. Your MCP server and tools should now be visible

---

## 📚 Project Structure
```
.
├── main.py            # Contains all core logic: tools, resources, prompts
├── notes.txt          # Local persistent storage for notes
└── README.md          # Project documentation
```

---

## 🎓 License

This project is licensed under the [MIT License](LICENSE).

---

## 🚀 Credits

Built with love using:
- [FastMCP](https://github.com/ai-collection/mcp)
- [uv](https://github.com/astral-sh/uv)
- Claude AI for seamless local testing

