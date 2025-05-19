# 🧠 Autonomous Stock Analysis using AI Agents

## 📘 Overview  
This project demonstrates how to build an AI-powered, multi-agent system that automates the analysis of company stocks. Using a coordinated agent framework, different AI roles work together to conduct web research, analyze financial reports, and generate insightful recommendations.

---

## 📂 Table of Contents  
- Framework Overview  
- How to Run  
- Project Structure & File Descriptions  
- Model Configuration Options  
- Using Local AI Models

---

## 🧠 Framework Overview  
The system operates through a team of specialized AI agents. Each agent is given a role (e.g., researcher, analyst, summarizer) and a goal. They collaborate to collect data, evaluate financial health, and form a final analysis. This approach is inspired by real-world task delegation among human experts.

---

## 🚀 How to Run

> ⚠️ By default, this project uses a cloud-based language model that may require paid access.

1. **Setup Environment Variables**  
   - Duplicate the `.env.example` file and rename it to `.env`.  
   - Fill in the necessary API keys for services like web search or financial document retrieval.

2. **Install Dependencies**  
   - Use the provided dependency manager (e.g., Poetry) to install required packages.

3. **Run the Program**  
   - Launch the main script and enter the name of the company to analyze when prompted.  
   - The agents will execute their tasks and return a structured report.

---

## 📁 Project Structure & File Descriptions

### `main.py`  
This is the main entry point of the project. It initializes the agents, sets up the task pipeline, and handles user input (the company name). Once run, it activates the full analysis process.

### `stock_analysis_agents.py`  
Defines the different AI agents used in the project. Each agent is configured with a role (e.g., market researcher, financial analyst), a backstory for context, and access to specific tools like calculators or search engines.

### `stock_analysis_tasks.py`  
Contains the workflow and task definitions that each agent is assigned. This script outlines how agents should collaborate step-by-step to complete the stock analysis process.

### `tools/` *(folder)*  
Includes various helper modules (tools) that the agents use to accomplish their tasks. These tools include:
- **Web Scraping**: For gathering real-time data from websites.  
- **Search Integration**: For querying the internet.  
- **Financial Document Search**: For fetching documents like 10-K or 10-Q filings.  
- **Calculators**: For computing financial ratios or basic math operations.

### `.env.example`  
A sample environment file showing all the keys and variables needed to run the project. Users should copy this file and rename it to `.env` before editing.

---

## ⚙️ Model Configuration Options

This project supports flexible model usage. By default, it uses GPT-4, but you can change it to any other model like GPT-3.5 or a locally hosted one.

To switch the model:
- Update the agent definition to reference the desired model during initialization.
- You can configure each agent individually, allowing a mix of model types in one workflow.

---

## 🖥️ Using Local AI Models (Ollama)

The system also supports local language models for users who want more control or need to run everything offline.

Steps:
- Install and configure the Ollama runtime environment.
- Set the desired local model as the agent's brain in the setup.
- Optionally tweak model behavior using configuration files (like setting stop words or adjusting temperature).

Using local models gives better privacy and allows customization for specific use cases.

---

