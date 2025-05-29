# LAMAA: LangGraph Multi-Agent Architecture

**LAMAA** is a powerful and modular **LangGraph-based multi-agent system** designed to automate complex workflows using intelligent collaboration between specialized agents. A central **Supervisor** agent manages six functional agents, each dedicated to a specific domain — enabling LAMAA to handle diverse tasks such as research, coding, shell operations, and weather reporting.

---

## 🧠 Architecture Overview

LAMAA includes **6 specialized agents**, each wrapped with error handling and managed by a central Supervisor:

| Agent Name         | Description |
|--------------------|-------------|
| `weather_agent`    | Fetches weather data using OpenWeatherMap API. |
| `math_agent`       | Performs basic BODMAS calculations. |
| `research_agent`   | Gathers information using the DuckDuckGo search engine. |
| `filesystem_agent` | Handles file operations like read, write, and listing files. |
| `shell_agent`      | Executes terminal commands in the current working directory. ⚠️ Use with caution — no regulatory sandboxing. |
| `python_agent`     | Executes Python code and returns the output. |

All agents, including the Supervisor, have built-in error handling to ensure graceful execution.

---

## 🚀 Capabilities Showcase

LAMAA can accomplish the following tasks:

- 📈 Generate a graphs for any real time data
- ☁️ Get current weather data for any city
- 📄 Create and write to a new file
- 🗃️ Add files to a GitHub repository using shell commands

---

## 📁 Project Structure

The entire implementation is provided in a **Jupyter Notebook (`LAMAA.ipynb`)** using the [LangGraph](https://github.com/langchain-ai/langgraph) framework. This allows interactive execution and modification of agent-based workflows.

---

## ⚙️ Installation

### 1. Clone the Repository

```bash
git clone https://github.com/mantis2404/LAMAA.git
cd LAMAA
```
### 2. Install Dependencies

Ensure Python 3.8+ is installed. Then, install the required packages:

```bash
pip install -r requirements.txt
```
### 3.🔐 Configure API Keys

Before using LAMAA, create a .env file in the root directory of the project and add the following variables:
```env
GOOGLE_API_KEY=your_google_api_key
OPENWEATHERMAP_API_KEY=your_openweathermap_api_key
MODEL="google_genai:gemini-2.0-flash"
```

You can change the model accordingly in the .env file

### 4.⚠️ Safety Notice

    ⚠️ The shell_agent can execute arbitrary shell/terminal commands in your current working directory.

    This feature is powerful but comes with security risks. It is currently unrestricted and does not use a sandbox.

    A Human-in-the-loop safety mechanism is under consideration for future versions to prevent accidental or harmful operations.

    Use with extreme caution.
    
---

## 🧩 Built With

- LangGraph
- OpenWeatherMap API
- Google Gemini
- DuckDuckGo Search

---

## 🤝 Contributing

Want to contribute? Awesome! You can:

- Add new agents (e.g., email, calendar, image generation)

- Improve agent accuracy and reliability

--- 

- Implement safety layers (sandboxing, approval prompts)

- Submit bug fixes and optimizations

Just fork the repo and open a pull request!
