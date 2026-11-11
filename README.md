# Blog Writing Crew

An AI-powered blog writing application built with **CrewAI** and **Streamlit**.

The project uses multiple AI agents to collaborate on creating blog posts. Instead of relying on one AI response, it divides the writing process into three stages: research, writing and editing.

## Features

- Enter a topic through a simple Streamlit interface.
- Research the given topic using an AI agent.
- Generate a structured blog post using a writing agent.
- Review and polish the draft using an editing agent.
- View the final blog post in the application.
- Download the generated blog post as a Markdown file.

## How It Works

The application uses three AI agents:

| Agent | Responsibility |
|---|---|
| Researcher | Collects relevant information and insights about the topic. |
| Writer | Creates an engaging, structured blog post using the research. |
| Editor | Reviews and improves the draft to produce the final post. |

The agents and their tasks are configured using YAML files.

## Tech Stack

- Python
- CrewAI
- Streamlit
- UV (dependency management)
- YAML (agent and task configuration)

## Project Structure

```text
blog_writing_crew/
│
├── src/
│   └── blog_writing_crew/
│       ├── config/
│       │   ├── agents.yaml
│       │   └── tasks.yaml
│       ├── tools/
│       ├── crew.py
│       └── main.py
│
├── fr.py
├── pyproject.toml
├── uv.lock
├── README.md
└── .gitignore
```

## Installation

**1. Clone the repository**

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
cd blog_writing_crew
```

**2. Install UV**

```bash
pip install uv
```

**3. Install project dependencies**

```bash
uv sync
```

**4. Configure your API key**

Create a `.env` file in the project root and add the API key required by your configured language model.

Keep your `.env` file private. Never upload API keys to GitHub.

## Run the Application

Start the Streamlit application from the project root:

```bash
uv run streamlit run fr.py
```

Open the local URL displayed in your terminal.

## Learning Goals

This project is an exploration of:

- Multi-agent collaboration using CrewAI.
- Defining agents and tasks using YAML.
- Connecting a Python application to an AI agent workflow.
- Building a user interface with Streamlit.
- Generating and downloading AI-created content.

## Future Improvements

- Improve research quality and source verification.
- Add more control over blog tone and writing style.
- Improve the user interface.
- Add options for different blog formats.

