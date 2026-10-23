# Activity — MCP server

**Course:** GitHub Copilot for Developers (IN2002)  
**Slides:** 305–317 in `GitHub Copilot for Developers Final - Notes.pptx`  
**Time:** about 25 minutes (Day 3, before Lab 8)  
**Difficulty:** Intermediate

**Objective:** Build a one-tool MCP server, start it from VS Code, and show that Copilot Chat calls the tool and returns `pong`.

**Code folder:** a new folder you create, named `mcp-hello`

MCP (Model Context Protocol) lets Copilot call a program outside the chat. In this activity that program is a small Python server. VS Code starts it, the server offers a tool named `ping`, and you ask Copilot to call that tool. The returned value is the string `pong`.

A reply that only says “pong,” with no tool call in the chat, means the model answered by itself. The activity is done when the chat shows a tool call for `ping` and the tool result is `pong`.

---

## Environment basics (read this first)

| Task | How |
| --- | --- |
| Open the activity | **File → Open Folder** on the `mcp-hello` folder you create below |
| Install | PowerShell in that folder: create `.venv`, then `python -m pip install fastmcp` |
| Server file | `server.py` at the root of `mcp-hello` |
| Launch config | `.vscode/mcp.json` |
| Start the server | **Start** on the `helloMcp2` entry inside `mcp.json` |
| Call the tool | Copilot Chat in **Agent** mode |

Use the Python inside `.venv`. The interpreter selected in VS Code and the `command` in `mcp.json` must be that same Python. A different Python produces `ModuleNotFoundError: No module named 'fastmcp'`.

Do not `print()` from `server.py`. This server talks to VS Code on standard input and output. A print on that channel breaks the connection.

---

## Steps from the training slides

Follow these steps in order. Slides 305–309 explain where servers come from and what tools, resources, and prompts are. The files you create start at slide 310.

### Step 1 — Create the workspace and install FastMCP

**Do this:**

1. Create a folder named `mcp-hello`.
2. **File → Open Folder** and open that folder. Trust it.
3. Open the terminal (**Ctrl+`**) and run:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install fastmcp
fastmcp version
```

4. Select the interpreter `.venv\Scripts\python.exe` (**Ctrl+Shift+P**, then **Python: Select Interpreter**).

**Expected result:** `fastmcp version` prints a FastMCP version, an MCP version, and a Python version. The status bar shows the `.venv` interpreter.

---

### Step 2 — Write the server

**Do this:** Create `server.py` in the root of `mcp-hello` with this code:

```python
from fastmcp import FastMCP

mcp = FastMCP("hello-mcp")

@mcp.tool
def ping() -> str:
    """Return pong. Use this to check that the MCP server is connected."""
    return "pong"

if __name__ == "__main__":
    mcp.run()
```

Save the file.

Slide 311 shows `from mcp.server.fastmcp import FastMCP`. That import does not match `pip install fastmcp` from slide 310. Use `from fastmcp import FastMCP`. `mcp.run()` starts the stdio transport the slide describes.

The docstring is the description Copilot reads when it decides whether to call `ping`.

**Expected result:** Explorer shows `mcp-hello/server.py`. The file imports `FastMCP`, defines `ping`, and calls `mcp.run()` only when the file is run directly.

---

### Step 3 — Tell VS Code how to start the server

**Do this:** Create `.vscode/mcp.json` with this content:

```json
{
  "servers": {
    "helloMcp2": {
      "type": "stdio",
      "command": "${workspaceFolder}/.venv/Scripts/python.exe",
      "args": ["${workspaceFolder}/server.py"]
    }
  }
}
```

Save the file.

The name `helloMcp2` matches slide 312. The slide’s `"command": "python"` often starts a Python that does not have FastMCP. This file starts the virtual environment’s `python.exe` instead.

The two files are separate jobs. `mcp.json` says how to launch the server. `server.py` is the server.

**Expected result:** Explorer shows this layout:

```text
mcp-hello/
  server.py
  .vscode/
    mcp.json
```

---

### Step 4 — Start the server

**Do this:**

1. Open `.vscode/mcp.json`.
2. Above the `helloMcp2` entry, click **Start**.
3. Read the toolbar: **Running**, **Stop**, **Restart**, a tool count, and **More**.

**Expected result:** The toolbar says **Running** and **1 tool**. That one tool is `ping`.

If the count is 0, or the server will not stay running, open **More** and read the log. After any later edit to `server.py`, click **Restart**. Saving the Python file does not reload a server that is already running.

---

### Step 5 — Call ping from Copilot Chat

**Do this:**

1. Open Copilot Chat (**Ctrl+Shift+I**).
2. Set the mode to **Agent**.
3. Open the tools list in the chat box and confirm `helloMcp2` and `ping` are enabled.
4. Send this message:

```text
Call the helloMcp2 ping tool now and show the actual tool result.
```

5. When Copilot asks to run the tool, read the request, then approve it.

**Expected result:** The chat shows a tool invocation for `ping`, and the tool result is `pong`. You approved the call. Copilot did not invent the word without a tool trace.

---

### Step 6 — Find other servers

**Do this:** Open [https://registry.modelcontextprotocol.io](https://registry.modelcontextprotocol.io) and search for one server you recognize, such as a source-control or documentation server. Read its description and which tools it exposes. Do not install it in this activity.

**Expected result:** You can name one published server, what it connects to, and at least one tool it offers. A registry listing is a catalog entry. It does not by itself mean the server is approved for work code.

---

## If you get stuck

- `ModuleNotFoundError: No module named 'fastmcp'`: the server was started with the wrong Python. In `mcp.json`, `command` must be `${workspaceFolder}/.venv/Scripts/python.exe`. Then click **Restart**.
- `ModuleNotFoundError: No module named 'mcp'`: the file still has the slide 311 import. Change the first line to `from fastmcp import FastMCP` and restart.
- The toolbar never appears: `mcp.json` is in `.vscode` at the root of the folder you opened, the top-level key is `servers`, and the folder you opened is `mcp-hello` itself.
- Chat replies “pong” and shows no tool call: stay in **Agent** mode, enable `ping` in the tools list, and send the Step 5 prompt again.
- The server stops as soon as it starts: remove any `print()` from `server.py`, save, and click **Restart**. Open **More** if it still stops.

## Success criteria

- [ ] `mcp-hello` is the folder you opened, and FastMCP is installed in `.venv`
- [ ] `server.py` imports `from fastmcp import FastMCP` and exposes `ping`
- [ ] `.vscode/mcp.json` starts that server with the `.venv` Python
- [ ] The `mcp.json` toolbar shows **Running** and **1 tool**
- [ ] Agent mode shows a real `ping` tool call, and the tool result is `pong`
- [ ] You can name one server from the MCP registry and one tool it exposes
