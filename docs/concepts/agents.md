## Understanding Sublayer Agents

Think of Sublayer Agents as your personal assistants, always ready to help with repetitive tasks or respond to changes in your environment. These agents can assist with a wide range of activities, from coding to data processing to system monitoring and beyond. You create an agent by defining four key aspects: what should wake it up (triggers), what it's trying to achieve (goal condition), how it checks its progress (check status), and what it actually does (step).

Triggers could be things like file changes, incoming data, time-based events, or even manual calls while the goal might be completing a data analysis or updating a system. The agent will keep checking its status and taking steps until it reaches its goal. It's like having a tireless helper that knows exactly when to jump in and what to do, making a variety of processes more efficient and responsive to change. Whether you're automating workflows, monitoring systems, or processing data, Sublayer Agents provide a flexible, event-driven approach to tackling complex and repetitive tasks.

### Customizing Banner Messages in Thor

With recent updates, Sublayer Agents now include a `banner` method for Thor command-line interface classes, allowing customization of the command name display in the `thor --help` output. This enhances user experience by clarifying the purpose of each command. Here's how you can incorporate it:

- **Custom Banner Method**: Add the `banner` method to your Sublayer agent classes to explicitly define the command name that will be displayed in help messages.
  
  ```ruby
  def self.banner
    "sublayer generate:agent"
  end
  ```

- **Example Usage**: This method improves the `thor --help` command output, helping users immediately understand what each command does by setting a clear and descriptive name.

  ```shell
  $ thor --help
  
  Commands:
    sublayer generate:agent    # Your defined banner here
    ...
  ```

- **Advantages**: Clear banner methods lead to better organized help outputs, enhancing usability and accessibility for anyone using the command-line interface apps built on Sublayer.

## Writing an Agent

Sublayer Agents are autonomous units of execution designed to perform specific tasks or monitor systems. They are built on top of the `Sublayer::Agents::Base` class and utilize a Domain Specific Language (DSL) for defining their behavior.

The DSL consists of four primary methods:

- `trigger`: Specifies events that activate the agent (e.g., file changes, time-based events, webhooks, etc.)
- `goal_condition`: Defines the criteria for task completion
- `check_status`: Evaluates the current state of the task
- `step`: Implements the actual logic to be executed

These methods work in concert to create a flexible, event-driven system for automating complex workflows and responding to changes in various environments.

## Try generating your own agent:

{% @iframe/iframe url="https://blueprints.sublayer.com/interactive-code-generator/sublayer-agents" %}

## Examples:

- [RSpecAgent](https://github.com/sublayerapp/sublayer/blob/main/spec/agents/examples/rspec_agent.rb)
  - A Sublayer agent that is triggered any time a test file or an implementation file changes with a goal of making the tests pass. When one of the files changes, the status is checked by running the tests. If the tests are failing, the agent sends the tests and the implementation to an LLM (using a [Sublayer::Generator](/concepts/generators)) to generate a new implementation that should pass the tests.