# Actions

Actions are responsible for performing specific operations to get inputs for a Generator or based on the generated output from a Generator. They encapsulate a single action and do not involve complex decision-making. Actions are the executable units that bring the generated inputs and output to life.

## Key Concepts of Actions

- **Encapsulation:** Each Action encapsulates a discrete piece of logic which is easy to manage and reuse.
- **Single Responsibility:** An Action should focus on a single task, be it retrieving information or making changes based on generated data.
- **Interaction with Generators:** Actions work alongside Generators to fetch necessary data and act on the results produced by Generators.

## Try making your own Action:

{% @iframe/iframe url="https://blueprints.sublayer.com/interactive-code-generator/sublayer-actions" %}

## Examples:

- [WriteFileAction](https://github.com/sublayerapp/tddbot/blob/43297c5da9445bd6c8882d5e3876cff5fc6b2650/lib/tddbot/sublayer/actions/write_file_action.rb): Writes text to a specified file. This action is a crucial part of the workflow when a Generator produces code that needs to be persisted.
- [RunTestCommandAction](https://github.com/sublayerapp/tddbot/blob/43297c5da9445bd6c8882d5e3876cff5fc6b2650/lib/tddbot/sublayer/actions/run_test_command_action.rb): Runs a test command on the command line returning the output. This action is used to verify generator outputs against expected results.
- [SpeechToTextAction](https://github.com/sublayerapp/rails_llm_voice_chat_example/blob/93300f268dde359b58c92a60db4b54d128d9d965/lib/sublayer/actions/speech_to_text_action.rb): Makes an API call to OpenAI's SpeechToText endpoint with audio data and returns text. Use this action to convert user input into textual data that can be further processed or used as input for Generators.
- [TextToSpeechAction](https://github.com/sublayerapp/rails_llm_voice_chat_example/blob/93300f268dde359b58c92a60db4b54d128d9d965/lib/sublayer/actions/text_to_speech_action.rb): Makes an API call to OpenAI's Speech Synthesis endpoint with text and returns audio data. Useful for converting generated text into audio responses in interactive voice applications.

### New additions:

- **Integration with AI Providers:** Actions now support interacting with multiple AI provider APIs (such as OpenAI, Claude, and Gemini) as part of their operations.
- **Support for SubLayer Agents:** Actions can contribute to or initiate processes managed by Sublayer Agents for enhanced automation and responsiveness in your applications.

By utilizing Actions in Sublayer, developers can streamline workflows and create applications that dynamically respond to the data processed by Generators, engaging in a rich interaction between generated content and execution logic.