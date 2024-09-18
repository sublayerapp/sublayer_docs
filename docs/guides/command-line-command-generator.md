## Command Line Command Generator

Browse the code on GitHub: [Command Line Command Generator](https://github.com/sublayerapp/clag)

Get the Gem on Rubygems: [CLAG](https://rubygems.org/gems/clag)

### Overview

The Command Line Command Generator is a Ruby gem that assists users in generating command-line commands based on a textual description, effectively streamlining repetitive command-line tasks for users. This tool is especially useful for those who use the command-line interface frequently but might not remember exact command syntaxes.

### Features

- **User-Friendly Command Generation**: Translates descriptions into actionable command-line commands.
- **Customization with Banner Method**: The newly added `banner` method provides a clear display of the command name in the `thor --help` output, enhancing user comprehension and navigation.
- **Flexible Model Selection**: As a model-agnostic tool, it allows users to select which AI model to use for generation, ensuring flexibility and adaptability. This includes the supported models like gpt-4, claude, and gemini among others.

### New Changes

#### Banner Method

With the recent update, the `banner` method was added to improve the usability and clarity of the generated commands in the `thor --help` output.
- **Purpose**: The `banner` method defines a custom command name display format. This makes it clearer which command is associated with the tool when using help features, thereby improving user experience.
- **Impact on CLI**: Existing commands will now have a more defined structure with distinct command names, making it easier to identify and utilize them.

#### Example Usage

To see how the `banner` affects the `thor --help` output, consider the following example:

```bash
$ thor help generate:action
```

Output:

```
Usage:
  sublayer generate:action

Options:
  ...

Description:
  ...
```

This output now distinctly showcases the actual command format as "sublayer generate:action," ensuring users are guided properly.

### How to Use

1. **Installation**
   Install the gem using the following command:
   ```bash
   gem install clag
   ```

2. **Running the Generator**
   Use a descriptive phrase to generate your desired command:
   ```bash
   clag "describe the command you want to generate"
   ```

3. **Getting Help**
   Access help for the command generator and see the improved banner usage:
   ```bash
   thor help clag
   ```

### Why Use the Banner Method?
- **User Experience**: Enhances the command-line help output, making it more intuitive.
- **Improved Navigation**: Facilitates easier navigation through command lists by providing meaningful descriptions and command identifiers.

### Future Updates

Stay tuned for more updates on this tool, as we continually strive to improve functionality and user experience, leveraging user feedback and advances in AI model capabilities.

