# Lab guides — GitHub Copilot for Developers (IN2002)

These guides walk through every hands-on lab in **GitHub Copilot for Developers Final - Notes.pptx**. Do the work in Visual Studio Code. The Python files live in `gh-copilot-devs-main`. This folder is only the written steps.

Open one lab README and follow it from top to bottom while that lab’s slides are on screen. Each step has the action from the slide and what you should see when it works.

| Guide | Slides | Day and time | Edit code in |
| --- | --- | --- | --- |
| [Lab 1 — Setup](lab-01-setup/README.md) | 39–47 | Day 1, 10:15–10:45 (30 min) | `gh-copilot-devs-main/Labs/Lab1` |
| [Lab 2 — Palindrome](lab-02-palindrome/README.md) | 81–87 | Day 1, 1:00–1:45 (45 min) | `gh-copilot-devs-main/Labs/Lab2` |
| [Lab 3 — Banking](lab-03-banking/README.md) | 102–110 | Day 1, 2:45–3:30 (45 min) | `gh-copilot-devs-main/Labs/Lab3` |
| [Lab 4 — Moby Dick](lab-04-moby-dick/README.md) | 178–183 | Day 2, 11:15–12:00 (45 min) | `gh-copilot-devs-main/Labs/Lab4` |
| [Lab 5 — Performance](lab-05-performance/README.md) | 197–209 | Day 2, 1:45–2:30 (45 min) | `gh-copilot-devs-main/Labs/Lab5` |
| [Lab 7 — Context](lab-07-context/README.md) | 257–264 | Day 3, 10:15–10:45 (30 min) | `gh-copilot-devs-main/Labs/Lab7` |
| [Activity — MCP server](activity-mcp/README.md) | 305–317 | Day 3, before Lab 8 (about 25 min) | A new `mcp-hello` folder you create |
| [Lab 8 — Prompt file](lab-08-prompt-file/README.md) | 319–325 | Day 3, 2:00–2:30 (30 min) | `gh-copilot-devs-main/Labs/Lab8` |
| [Lab A1 — Accounts receivable](lab-a1-accounts-receivable/README.md) | 346–351 | Optional self-study (about 60 min) | A new folder you create |

There is no Lab 6. After Lab 5 the deck teaches documentation, then the next hands-on is Lab 7.

## How to run a lab

1. Open the lab README.
2. In VS Code choose **File → Open Folder** and open the code folder in the table. Copilot uses the open folder as the project. Open `Lab4`, for example, rather than the whole `gh-copilot-devs-main` repo, when the guide says to.
3. If VS Code asks whether you trust the folder, choose **Yes, I trust the authors**. Restricted mode limits Copilot.
4. Do the steps in order. Read the suggestion before you accept it. Two people often get different code for the same comment, and both can be acceptable if the behavior matches the expected result.
5. Tick the success criteria at the bottom before you leave the lab.

## Shared controls

| You want to | Do this |
| --- | --- |
| Accept gray ghost text | Pause, then press **Tab** |
| Dismiss ghost text | Keep typing, or press **Escape** |
| See another suggestion | Hover the ghost text and use the arrows |
| Open Inline Chat | **Ctrl+I** |
| Open the Chat view | Chat icon at the top right, or **Ctrl+Shift+I** |
| Open Extensions | **Ctrl+Shift+X** |
| Open the terminal | **Ctrl+`** (PowerShell) |
| Attach a file in Chat | Type `#file` and pick the file, or `#` then the file name |
| Attach the whole project | Type `#codebase` and pick it from the list |
| Attach the terminal | Type `@terminal` and pick it from the list |
| Run a saved prompt | Type `/` and the prompt name |

Sign in with the **GitHub** account for this class. A Microsoft account sign-in is a different login and does not activate Copilot.

The virtual machine is removed at the end of class. Copy any file you want to keep before the last day ends. Keep real passwords and API keys off the machine and out of prompts.
