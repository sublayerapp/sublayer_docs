# Generators

Generators are responsible for generating specific outputs based on input data. They focus on a single generation task and do not perform any actions or complex decision-making. Generators are the building blocks of the Sublayer framework.

## New Feature: Sublayer Agent Generator

The latest update introduces a new command within the Sublayer framework: the `sublayer generate agent` command. This command allows developers to generate a Sublayer Agent based on specific criteria such as description, provider, model, triggers, goal, check status, and step methods. These agents are autonomous units designed to perform specific tasks or monitor systems, and they are written using a specialized Domain Specific Language (DSL) designed for this purpose.

### Writing an Agent

Sublayer Agents are created using the new `SublayerAgentGenerator` class, which generates agents following this structure:

- **Description:** A brief overview of what the agent is intended to do.
- **Trigger:** Defines what starts the agent's operations (e.g., file changes, manual calls).
- **Goal Condition:** Describes what the agent is trying to achieve.
- **Check Status:** Method to evaluate the agent's progress towards its goal.
- **Step:** Defines the actions the agent will perform repeatedly until it achieves its goal.

### Generating Sublayer Agents with the Command

To generate a new agent using the command, run:

```
sublayer generate agent --description "<agent_description>" --provider "<AI_provider>" --model "<AI_model>" 
```

The command will prompt for additional details such as the triggering condition, the specific steps the agent should follow, and how it should check its progress.

### Examples

The following examples illustrate how you might use the `sublayer generate agent` command:

1. **Monitoring File Changes**: Generate an agent monitoring a folder for new files and processing each file according to specified rules.
2. **Data Processing**: Create an agent that processes batches of data and uploads results to a database once complete.
3. **Continuous Integration/Deployment**: Agents can be used to automate parts of the CI/CD pipeline, such as running tests or deploying updates.

### Learn More

To understand more about Sublayer Agents, visit the [Agents Documentation](/docs/concepts/agents.md). You can also refer to our tutorials that demonstrate real-world examples of agent creation and use-cases, which provide deeper insights and practical experiences working with this innovative feature.

By introducing the ability to generate Sublayer Agents, the Sublayer framework extends its functionality, providing a more robust tool for automating and managing complex tasks driven by AI.

### Try Creating Your Own Generator:

{% @iframe/iframe url="https://blueprints.sublayer.com/interactive-code-generator/sublayer-generators?example=true" %}

### [Examples](https://github.com/sublayerapp/sublayer/tree/main/examples):
- **CodeFromDescriptionGenerator**: Generates code based on a description and the technologies used.
- **DescriptionFromCodeGenerator**: Generates a description of the code passed in to it.
- **CodeFromBlueprintGenerator**: Generates code based on a blueprint, a blueprint description, and a description of the desired code.
