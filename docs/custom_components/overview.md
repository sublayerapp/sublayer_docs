## Sublayer Custom Components Overview

The Sublayer framework is designed to be extensible and customizable. Beyond building your own Generators, Actions, and Agents, you can also create custom Output Adapters for your Generators, Triggers for your Agents, and Providers for any custom model you're working with.

### Output Adapters
- Learn more about creating your own custom output adapter in [Output Adapters](/docs/custom_components/output-adapters.md).

### Custom Triggers
- You can create custom triggers to define specific conditions under which an agent will act. Refer to [Triggers](docs/concepts/triggers.md) for more examples and information.

### Custom Generators
- Generators are responsible for generating specific outputs based on input data. Read more about them in [Generators](/docs/concepts/generators.md).

### Custom Agents
- Agents automate workflows by continuously checking status and taking steps toward a goal condition. Read more about them in [Agents](/docs/concepts/agents.md).

### Introducing SublayerAgentGenerator
- With the newly added `SublayerAgentGenerator`, you can now generate custom Sublayer agents efficiently. This tool allows developers to automate the creation and management of agents based on specific criteria, enhancing productivity and consistency within projects. Learn more about this in the [Custom Components](docs/guides/command-line-command-generator.md) section.

### Adding New AI Providers
- Customize and expand your project's capabilities by integrating various AI providers. For details on supporting different AI providers, refer to [Advanced Configurations](/docs/advanced_config.md).

This extensive support for customization ensures that your integration and development processes remain streamlined and tailored to your specific needs, allowing for the rapid development of complex functionalities without starting from scratch.