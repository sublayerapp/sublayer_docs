We're always looking for more ideas for guides. If you have an idea for a guide, let us know by sending us a message in [our Discord](https://discord.gg/pWZ689GW7U).

## List of Guides

### [Rails Voice Chat with LLM](/docs/guides/voice-chat.md)

A Ruby on Rails app that uses OpenAI's Speech to Text and Text to Speech APIs to enable voice chatting with an LLM.

* Learn how to use Actions and Generators
* Learn how to use a simple conversational context with a Generator

### [TDD Bot](/docs/guides/tdd_bot.md)

A command line program that uses an LLM to generate code to pass your failing tests, enabling a workflow where you practice Test-Driven Development with an LLM.

* Learn how Tasks are used to combine Actions and Generators
* Learn how to build different types of Actions
* Learn how a Generator can take multiple inputs to generate the output you want

### [Run LLM Models Locally with Llamafile](/docs/guides/running-local-models-with-llamafile.md)

A guide on the recommended way to set up and run LLMs locally to interface with Sublayer.

* Learn how to set up [llamafile](https://github.com/Mozilla-Ocho/llamafile)
* Learn which models we recommend for local use
* Learn how to point Sublayer to your locally running server

### [Command Line Command Generator](/docs/guides/command-line-command-generator.md)

A Ruby command line gem that lets you describe something you'd like to do on the command line, generates a command for you, and stores it in your clipboard.

* Learn how to use Generators
* Learn how to take advantage of Sublayer being model-agnostic and allow users to select which model to use
* Try the Gem out yourself on [Rubygems](https://rubygems.org/gems/clag)

### [Run Llama3.1 Locally with Ollama](/docs/guides/running-local-llama31-with-ollama.md)

Learn how to run Llama 3.1 with Ollama locally.

* Install Ollama and learn how to use it to run models locally
* Set up a custom provider in Sublayer to utilize Llama 3.1
* Explore a full demo project using Llama 3.1

### [Build a Custom Trigger](/docs/guides/build-a-custom-trigger.md)

Learn how to build a custom trigger that defines when an agent performs its tasks.

* Create a time interval trigger for an agent
* Understand the flexibility of triggers in agent operation

### [Build a Custom Sublayer Agent](/docs/guides/build-custom-agent.md)

Learn to create custom agents that leverage the new Sublayer agent framework.

* Understand the four main components: triggers, goal condition, check status, step
* Explore practical examples using different AI providers
* Integrate custom agents into existing applications

This newly added guide will help users understand how to leverage the recently introduced sublayer agent feature and customize it to suit specific needs within their projects.