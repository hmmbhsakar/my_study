---
title: "Agent Development Kit"
tags: [Google, ADK, Agentic AI, Agent]
---

## TL;DR

Agent Development Kit (ADK) is a flexible, and modular open-source framework for developing, evaluating and deploying sophisticated AI agents with code-first flexibility for greater control. While optimized for Gemini and the Google ecosystem, ADK is model-agnostic, deployment-agnostic, and is built for compatibility with other frameworks. Building complex, production-ready AI agents, especially multi-modal, multi-agent systems. ADK was designed to make agent development feel more like software development, complete with native multi-modal streaming and easy local debugging via a built-in UI, to make it easier for developers to create, deploy, and orchestrate agentic architectures that range from simple tasks to complex workflows.

## Important Info

- [Documentation Link](https://google.github.io/adk-docs/)
- [ADK Sample Agents](https://github.com/google/adk-samples)
- [Github Repo Python](https://github.com/google/adk-python)

## Features

### Main Highlights

- Variations
  - Python SDK
  - Java SDK
- open foundation
  - model agnostic: Can run with any model of choice
  - deployment agnostic: Can run locally or on google cloud or on whichever infra wanted.
  - interoperability: easily integrate agents with existing tools and services, or even with agents that are built on other frameworks.
- Ways to Build Agent
  - Config based
  - Code based 
- Built-in tools
  - Google search
- Multi-Model Streaming: Native Bi directional real-time audio and video streaming
  - Agents that can hear, can see and respond in real time.
  - Truly Interactive and real-time agent experiences
- UI Playground: 
  - Why: It required a lot of setup to just test and debug the agent locally. Developers wanted to iterate quickly without spinning up a ton of complex dependencies.

### Core Principles

- Make agent development feel like software development. 
  - Built ADK using familiar software engineering practices, just like regular classes or functions. 

### Agent Definition

- Standard ADK agent Class
- 

### UI Playground

- `adk web`: launch a UI locally to test, visualize and debug agent.
- Event Tab: shows the agent's workflow and how it decided to use the subagent.
- Request and Response Tabs: Gives the step-by-step trace, so we know what data goes where. 
- Native bi-directional audio video streaming: Agent can hear and see input. It is built in, no extra libraries for the basic setup. 

### Code Structure and Component

- Importing ADK required libraries
- Definitions of sub-agents
- Definition of the root agent
- Run the root agent from the Runner
