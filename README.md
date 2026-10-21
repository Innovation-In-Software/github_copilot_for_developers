# GitHub Copilot for Developers (IN2002)

Topics covered in **GitHub Copilot for Developers Final.pptx**: 369 slides across 8 core modules, 2 appendix modules and 9 hands-on labs.

Instructor: Dr. Gurinderjeet Kaur

Slide numbers are given in brackets.

---

## Timetable – October 21–23, 2026 (8:00 AM – 4:00 PM)

Each day has two 15-minute tea breaks (10:00 and 2:30) and a one-hour lunch (12:00).

### Day 1 – Wednesday, October 21

| Time | Session | Slides |
|------|---------|--------|
| 8:00 – 8:30 | Welcome, logistics and introductions | 1–4 |
| 8:30 – 10:00 | Introduction to GitHub Copilot: generative AI, LLMs, use cases, IDEs, licensing, agenda | 5–38 |
| **10:00 – 10:15** | **Tea break** | |
| 10:15 – 10:45 | **Lab 1** – Setup | 39–47 |
| 10:45 – 12:00 | Module 1 – Fundamentals: context, 3-in-1 model, workflow, privacy, settings | 48–80 |
| **12:00 – 1:00** | **Lunch** | |
| 1:00 – 1:45 | **Lab 2** – Palindrome | 81–87 |
| 1:45 – 2:30 | Module 2 – Inline Suggestions: ghost text, context, toolbar, inline chat | 88–101 |
| **2:30 – 2:45** | **Tea break** | |
| 2:45 – 3:30 | **Lab 3** – Banking Application | 102–110 |
| 3:30 – 4:00 | Day 1 recap and Q&A | |

### Day 2 – Thursday, October 22

| Time | Session | Slides |
|------|---------|--------|
| 8:00 – 8:15 | Day 1 recap | |
| 8:15 – 10:00 | Module 3 – Copilot Chat (part 1): chat views, configuration, modes, permissions, checkpoints, model selection | 111–152 |
| **10:00 – 10:15** | **Tea break** | |
| 10:15 – 11:15 | Module 3 – Copilot Chat (part 2): variables, `#` context, slash commands, shortcuts | 153–177 |
| 11:15 – 12:00 | **Lab 4** – Moby Dick | 178–183 |
| **12:00 – 1:00** | **Lunch** | |
| 1:00 – 1:45 | Module 4 – Common Tasks: logic errors, error handling, syntax errors | 184–196 |
| 1:45 – 2:30 | **Lab 5** – Performance | 197–209 |
| **2:30 – 2:45** | **Tea break** | |
| 2:45 – 3:30 | Module 5 – Code Documentation | 210–228 |
| 3:30 – 4:00 | Kahoot quiz, Day 2 recap and Q&A | |

### Day 3 – Friday, October 23

| Time | Session | Slides |
|------|---------|--------|
| 8:00 – 8:15 | Day 2 recap | |
| 8:15 – 10:00 | Module 6 – Advanced: tokens, AI Credits, context window, semantic index, `@` participants | 229–256 |
| **10:00 – 10:15** | **Tea break** | |
| 10:15 – 10:45 | **Lab 7** – Context | 257–264 |
| 10:45 – 12:00 | Module 7 – Customization (part 1): prompt files, instructions, skills, tool sets, hooks, custom agents | 265–302 |
| **12:00 – 1:00** | **Lunch** | |
| 1:00 – 2:00 | Module 7 – Customization (part 2): Model Context Protocol (MCP) | 303–318 |
| 2:00 – 2:30 | **Lab 8** – Prompt File | 319–326 |
| **2:30 – 2:45** | **Tea break** | |
| 2:45 – 3:30 | Appendix A2 – Managing GitHub Repositories: commits, PRs, code reviews | 352–368 |
| 3:30 – 4:00 | Course wrap-up, Q&A and evaluations | |

*Appendix A1 (Agile Methodologies and Lab A1, slides 327–351) is optional. Cover it if time allows, or assign it as self-study.*

---

## Course Introduction (slides 1–38)

- Logistics, instructor and class introductions (2–4)
- What a "copilot" is and what GitHub Copilot does (5–6)
- **Pop quiz:** lines of code before an error (7)
- AI assistants as pair programmers, with the developer in charge (8–9)
- Who's driving? Over-reliance on automation (10)
- GitHub and OpenAI: the origins of Copilot (11)
- Generative AI and how Copilot predicts code (12–14)
- **Pop quiz:** why pause during code completion (15)
- LLMs vs SLMs, training sources and data staleness (16–18)
- Why AI output needs code review: hallucinations, bias, staleness and security risks (19–20)
- Copilot Chat overview (21)
- Use cases: scaffolding, completion, error handling, learning new languages, TDD, finding logic errors and source control (22–25)
- Copilot is extensible (26)
- LLM model families available in Copilot (27)
- Supported languages and IDEs, and Visual Studio Code (28–30)
- GitHub account and Copilot license plans (31–32)
- ChatGPT vs GitHub Copilot (33–34)
- Course agenda, labs and class expectations (35–37)
- Productivity research findings (38)

### Lab 1 – Setup (slides 39–47)
- Virtual machine assignment and environment setup
- Verify the Copilot extensions and sign in
- Create a lab folder and a Python file
- Trigger and accept the first Copilot suggestion

---

## Module 1 – Fundamentals: Details and Workflow (slides 48–80)

- Copilot as a cloud-based generative AI tool (50)
- Prompts and context: what Copilot actually sends (51–53)
- The 3-in-1 model: fill-in-the-middle, Next Edit Suggestions and long-distance edits (54–56)
- The Copilot workflow, in five steps from prompt to results in the IDE (57–60)
- Licensed content and public-code matching (62)
- Privacy, security and sensitive data in prompts (63–65)
- Scope of suggestions: file, project, prompt and language scope (66–67)
- Settings and configuration (68):
  - Privacy settings on GitHub.com and in the status menu (69–71)
  - Enabling and disabling inline suggestions globally and per language (72–76)
  - Snoozing inline suggestions (77)
  - The completions panel (78)
  - Copilot settings in VS Code (79)
- Retrospective (80)

### Lab 2 – Palindrome (slides 81–87)
- Generate an `is_palindrome` function from a comment
- Generate a `main` test function and run it
- Add and test an `is_prime` function

---

## Module 2 – Inline Suggestions: Basics and Best Practices (slides 88–101)

- Getting started with code completion (90)
- Ghost text: predicting, accepting, ignoring and cycling suggestions (91)
- Providing context through names, comments, docstrings and imports (92–93)
- Partial code guidance (94)
- The inline suggestion toolbar: Accept, Accept Word, Accept Line and Always Show Toolbar (95–96)
- The inline chat window and the Keep/Undo diff view (97–99)
- Best practices for inline suggestions (100)
- Retrospective (101)

### Lab 3 – Banking Application (slides 102–110)
- Build pure functions with ghost-text suggestions: `deposit`, `loan`, `withdrawal` and `loan_payment`
- Enhance them with transaction messages
- Generate a `main` function to test the application

---

## Module 3 – Copilot Chat Integration (slides 111–177)

- Opening Copilot Chat: the Chat view and its keyboard shortcuts (113)
- Chat view menu (114–119):
  - Inline chat and Quick Chat
  - New chat window and new chat editor
  - Managing settings
  - Open in Agents
- Configuring inline suggestions (120–128):
  - Status, the completions panel and keyboard shortcuts
  - Custom key bindings
  - Diagnostics and logs
  - Documentation links
- Modes: Interactive, Plan and Autopilot (129–131)
- Permissions: manual, assisted and allow-all, plus terminal sandboxing (132–134)
- Agent role picker: Agent, Ask and custom agents (135)
- Action bar: Apply, Insert, Copy, Insert into Terminal and Insert into New File (136–137)
- Checkpoints: restoring and forking conversations (138–140)
- Changed-files summary and the diff view (141–143)
- Other features (144–152):
  - Auto model selection, HydraFusion, and the Efficiency, Balance and Intelligence settings
  - Choosing a specific model vs Auto
  - **Pop quiz:** choosing a specific model while Auto is selected (151)
- Variables and disambiguating prompts (153–156)
- Context references: the Add Context button, `#file`, `#selection` and `#codebase` (157–161)
- Slash commands: `/fix`, `/explain`, `/tests`, `/fixtestfailure`, `/new` and `/clear` (162–172)
- **Pop quiz:** are `/fix` and a "fix" prompt the same? (173–174)
- Chat input box anatomy and shortcut keys (175–176)
- Retrospective (177)

### Lab 4 – Moby Dick (slides 178–183)
- Text processing with Copilot Chat: count lines, words and characters
- Revise the script:
  - Handle empty and missing files
  - Add timing and command-line arguments
- Generate unit tests with `/tests` (unittest)

---

## Module 4 – Common Tasks: Error Handling, Syntax Checking and More (slides 184–196)

- Logic errors: modifying a list while iterating over it (186–188)
- **Pop quiz:** syntactical or logical error? (187)
- Generating error handling with try/except (189–191)
- Fixing syntax errors across languages (192)
- Silent logic errors that run but give wrong results (193–195)
- Retrospective (196)

### Lab 5 – Performance (slides 197–209)
- Analyze the time complexity of `find_duplicates`
- Improve the algorithm, then test it against different input types
- Python generics and type hints
- Example prompts
- **Bonus:** benchmarking

---

## Module 5 – Code Documentation (slides 210–228)

- Context-aware documentation generation (212)
- Why developers avoid documentation, and documentation as part of code quality (213–214)
- Where to document: docstrings, module summaries, READMEs and API docs (215)
- High-quality comments in Google, NumPy and Javadoc styles (216)
- Reverse engineering unfamiliar code (217)
- Writing READMEs and API documentation (218–219)
- Architectural summaries (220)
- Keeping documentation current during refactoring (221)
- Risks and limitations of AI-generated documentation (222)
- Advanced prompts and best practices: `#selection`, `#file` and prompt-file templates (223–226)
- Retrospective (227)

---

## Module 6 – Advanced: Setup, Reference and More (slides 229–264)

- Tokens and GitHub AI Credits (231–236):
  - Billing
  - Ghost text is included in every plan
  - Per-model token pricing
  - A worked cost example
- Chat messages vs tokens (237–238)
- Viewing credit usage in the status menu (239)
- What tokens are and why they matter (240–243)
- The context window, and how to reduce token usage (244–247)
- The Codebase Semantic Index (248–253):
  - Indexing order of preference
  - Exclusions
  - Rebuilding the index
- Chat participants `@terminal`, `@vscode` and `@github` (254–255)
- Retrospective (256)

### Lab 7 – Context (slides 257–264)
- Use `#codebase` to understand a Python project and run it
- Use `@terminal` to diagnose and fix command errors

---

## Module 7 – Customization: Prompts, Instructions and MCPs (slides 265–325)

- The Open Customization menu (267)
- Prompt files (268–274):
  - Reusable `.prompt.md` files
  - Front matter: `agent`, `applyTo` and `priority`
  - The prompt body
  - Running prompts with slash commands
- Delegating sessions: Copilot, Local, Cloud, Claude and Codex (275–276)
- Instructions and rules (277–284):
  - `copilot-instructions.md`
  - `*.instructions.md` with `applyTo`
  - `AGENTS.md`
  - Instruction templates
- Custom instructions do not affect ghost text (281)
- Skills: features, capabilities, setup and an example `skill.md` (285–289)
- Tool sets (290)
- Hooks (291–297):
  - Features and actions
  - Setup and JSON files
  - Hook event keywords
- Custom agents: `.github/agents/*.agent.md`, setup steps and testing (298–302)
- Model Context Protocol (MCP) (303–317):
  - MCP servers, where to find them and the protocol (USB-C analogy)
  - FastMCP: features, installation and sample server code
  - `mcp.json` configuration and project structure
  - Starting and running an MCP server and calling its tools
  - MCP registries and galleries
- Retrospective (318)

### Lab 8 – Prompt File (slides 319–325)
- Create a custom `.prompt.md` file with front matter
- Generate bubble sort, insertion sort and merge sort functions
- Run the prompt as a slash command and test the result

**Course completion (326)**

---

## Appendix A1 – Agile Methodologies: Scrum, Use Cases and Sprint Backlog (slides 327–351)

- Agile methodology, roles and practices: Scrum, Kanban, XP and SAFe (329–331)
- User stories, use cases and Gherkin (Given–When–Then) (332–334)
- The Scrum workflow (335)
- Copilot in Agile, end to end (336–344):
  - User story → acceptance criteria → GWT
  - Failing unit tests (TDD) → minimal implementation
- Retrospective (345)

### Lab A1 – Accounts Receivable (slides 346–351)
- Convert user stories into acceptance criteria and GWT scenarios
- Generate unittest tests from the GWT file
- Implement minimal production code and run the test suite

---

## Appendix A2 – Managing GitHub Repositories: Commits and Pull Requests (slides 352–368)

- Repository management with Copilot (354)
- Commit messages and best practices, including Conventional Commits (355–359)
- Pull request descriptions (360–361)
- Improving code reviews (362–363)
- Branch name suggestions (364–365)
- Repository documentation: README, CONTRIBUTING and templates (366–367)
- Retrospective (368)

---

## Labs at a Glance

| Lab | Topic | Slides |
|-----|-------|--------|
| Lab 1 | Setup: verify Copilot in VS Code | 39–47 |
| Lab 2 | Palindrome and `is_prime` with ghost text | 81–87 |
| Lab 3 | Banking application | 102–110 |
| Lab 4 | Moby Dick text processing with Copilot Chat | 178–183 |
| Lab 5 | Algorithm performance and generics | 197–209 |
| Lab 7 | Context with `#codebase` and `@terminal` | 257–264 |
| Lab 8 | Custom prompt file | 319–325 |
| Lab A1 | Accounts Receivable: user stories → GWT → TDD | 346–351 |

*Pop quizzes appear on slides 7, 15, 25, 151, 173 and 187.*
