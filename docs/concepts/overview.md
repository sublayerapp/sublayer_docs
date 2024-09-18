## Framework Guide

Using Generators, Actions, and Agents

- [Generators](/docs/concepts/generators.md)
- [Triggers](/docs/concepts/triggers.md)
- [Actions](/docs/concepts/actions.md)
- [Agents](/docs/concepts/agents.md)

## Banner Method in Commands

In recent updates, a `banner` method has been added to several classes within the `lib/sublayer/cli/commands` directory. This method plays a pivotal role in displaying clear and informative command names when using the Thor CLI framework. Here's how it enhances your command-line experience:

- **Purpose of the Banner Method:** The `banner` method customizes the display of command names in help messages, offering a more descriptive and organized view of available commands.
- **Example Output:** When you use `thor --help`, you will now see improved command names such as `sublayer generate:agent`, `sublayer generate:action`, `sublayer generate:generator`, and `sublayer new PROJECT_NAME.`
- **Implementation:** This method has been added to the `action.rb`, `agent.rb`, `generator.rb`, and `new_project.rb` files. It ensures users gain immediate understanding of command usage during help calls.

## Benefits of the Banner Method

- **User Experience Improvement:** By displaying clear command names, users find it easier to navigate and understand the functionality available through the CLI.
- **Organizational Clarity:** Commands are categorized clearly, reducing confusion and improving documentation consistency.

This update reflects an ongoing commitment to improving user interaction and experience within the Sublayer framework, making it more intuitive and accessible for developers.