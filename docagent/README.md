# Docagent Crew

Welcome to the Docagent Crew project, powered by [crewAI](https://crewai.com). This template is designed to help you set up a multi-agent AI system with ease, leveraging the powerful and flexible framework provided by crewAI. Our goal is to enable your agents to collaborate effectively on complex tasks, maximizing their collective intelligence and capabilities.

## Installation

Ensure you have Python >=3.10 <3.14 installed on your system. This project uses [UV](https://docs.astral.sh/uv/) for dependency management and package handling, offering a seamless setup and execution experience.

First, if you haven't already, install uv:

```bash
pip install uv
```

Next, navigate to your project directory and install the dependencies:

(Optional) Lock the dependencies and install them by using the CLI command:
```bash
crewai install
```
### Customizing

**Add your `OPENAI_API_KEY` into the `.env` file**

- Modify `src/docagent/config/agents.yaml` to define your agents
- Modify `src/docagent/config/tasks.yaml` to define your tasks
- Modify `src/docagent/crew.py` to add your own logic, tools and specific args
- Modify `src/docagent/main.py` to add custom inputs for your agents and tasks

## Running the Project

To kickstart your crew of AI agents and begin task execution, run this from the root folder of your project:

```bash
$ crewai run
```

This command initializes the docagent Crew, assembling the agents and assigning them tasks as defined in your configuration.

This example, unmodified, will run the create a `report.md` file with the output of a research on LLMs in the root folder.

## Understanding Your Crew

The docagent Crew is composed of multiple AI agents, each with unique roles, goals, and tools. These agents collaborate on a series of tasks, defined in `config/tasks.yaml`, leveraging their collective skills to achieve complex objectives. The `config/agents.yaml` file outlines the capabilities and configurations of each agent in your crew.


## Steps followed

1) python3.12 is installed. Use crewai for demo project, Install create project: "crewai create crew docagent"
2) Enable virtual environment and update .env file with required ollama version
3) start ollama - "ollama serve" , this process should be running before you run "crewai run"
4) prepare your internal documentation and upload your pdf files under knowledge directory.
5) update config/agents.yaml and config/tasks.yaml with your tool details
6) update agent detail, input variables..etc  and train the model using main.py and crew.py
7) crewai install to install all the dependancies.
8) crewai run to launch your doc agent for questions and answers...
