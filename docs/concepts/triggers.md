A trigger is an activation mechanism in an agent that determines when an agent performs its tasks. Triggers can respond to various events or conditions (changes in files, time intervals, or any external inputs) providing flexibility in how and when agents operate. By defining custom triggers, developers can create agents that react dynamically or execute tasks on precise schedules.

## Banner Method for Sublayer Commands

Recently, a `banner` method has been added to the classes within the Sublayer CLI commands. This method provides a customized banner description for each command, enhancing the `thor --help` output by clearly showing the command's use. This improves usability and user experience by providing direct and specific guidance.

### Usage Example

For instance, for the class handling agent commands, the `banner` method usage looks as follows:

```ruby
def self.banner
  "sublayer generate:agent"
end
```

When you run `thor --help`, you'll see the command name effectively displayed as `sublayer generate:agent`, making the command-line tool's navigation more intuitive.

### Benefits

- **Improved Clarity:** The `banner` method adds clarity to what each command does within the tool.
- **User Guidance:** It precisely guides users by displaying custom command-line descriptions.
- **Workflow Enhancement:** Helps prevent confusion or errors in selecting or using commands.

For users who want to implement similar features in their CLI tools, customizing banners in this way can significantly improve the interface with relatively simple code changes.

## Try making your own trigger:

{% @iframe/iframe url="https://blueprints.sublayer.com/interactive-code-generator/sublayer-triggers" %}

## Examples:

- [FileChange](https://github.com/sublayerapp/sublayer/blob/main/lib/sublayer/triggers/file_change.rb): Activate agent when a file has changed.