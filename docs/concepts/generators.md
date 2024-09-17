# Generators

Generators are crucial components in the Sublayer framework, tasked with generating specific outputs based on input data. They are focused on solving a single generation problem and do not engage in complex decision-making or actions; instead, they serve as the building blocks for complex workflows when combined with Actions, Agents, and Tasks in Sublayer.

## Key Features

- **Modular Design:** Generators are designed to be modular, making it easy to plug different generators together or swap them out as needed.
- **LLM Integration:** Generators typically leverage Language Learning Models (LLMs) like GPT-4 to transform given inputs into the desired outputs through well-defined prompts.

## Creating Your Own Generator

To create a generator, you'll usually define a class that inherits from `Sublayer::Generators::Base`, and specify how the generator should process inputs to produce output through implementing the `prompt` and `generate` methods.

### Example: Code Generator

Here's a simple example of a generator that takes a description of a task and the technologies to use, and produces code using an LLM:

```ruby
# ./code_from_description_generator.rb

require "sublayer"

module Sublayer
  module Generators
    class CodeFromDescriptionGenerator < Base
      llm_output_adapter type: :single_string,
                         name: "generated_code",
                         description: "The generated code in the requested language"

      def initialize(description:, technologies:)
        @description = description
        @technologies = technologies
      end

      def generate
        super
      end

      def prompt
        <<-PROMPT
          You are an expert programmer in \\#{@technologies.join(", ")}.

          Task description: \\#{@description}

          Goal: Generate code using the following technologies: \\#{@technologies.join(", ")}.
        PROMPT
      end
    end
  end
end
```

### Using a Generator

To utilize this generator, you instantiate it with the required inputs and call `generate`:

```ruby
require './code_from_description_generator'
generator = Sublayer::Generators::CodeFromDescriptionGenerator.new(description: 'A calculator function', technologies: ['Ruby'])
puts generator.generate
```

### Advanced Configuration

For configuring LLMs and integrating specific AI models, please refer to the advanced configuration guide on setting up providers and models in the [Advanced Config](docs/advanced_config.md) section.

## Built-in Generators

Sublayer comes with several built-in generators which can be found and referenced as examples:

- [CodeFromDescriptionGenerator](https://github.com/sublayerapp/sublayer/blob/main/examples/code_from_description_generator.rb): Generates code based on a description.
- [DescriptionFromCodeGenerator](https://github.com/sublayerapp/sublayer/blob/main/examples/description_from_code_generator.rb): Creates a description from a given block of code.
- [TranscriptionSummarizerGenerator](https://github.com/sublayerapp/sublayer/blob/main/examples/transcription_summarizer.rb): Summarizes transcription files and provides structured outputs.

## Tips for Effective Generator Design

- **Clear and Detailed Prompts:** The more precise your prompt, the more accurate the output from your LLM.
- **Iterative Testing:** Test your generator in various scenarios to ensure robustness.
- **Integration with Other Components:** Consider how your generator will interact with Actions, Agents, and the overall system to maximize efficiency and utility.

## Conclusion

Generators are flexible and powerful tools within the Sublayer framework, designed to efficiently handle specific generative tasks, thus enabling more complex application development workflows. For a deep dive into making the most of Sublayer's capabilities, check out our [comprehensive guides and examples](docs/guides/overview.md).