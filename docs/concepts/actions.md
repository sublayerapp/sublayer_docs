Actions are the building blocks within the Sublayer framework that execute specific tasks. They bridge the gap between the desired outcome set by Generators and the practical steps needed to achieve that outcome. Actions are responsible for performing operations to get inputs for a Generator or based on the generated output from a Generator. They encapsulate a single action and are not intended for complex decision-making. Instead, they act as the executable units that bring the generated data to life.

## New Feature: `banner` Method

With the recent update, a new `banner` method has been introduced in Actions classes. This method defines the display text that appears when using the `thor --help` command, enhancing the user's understanding of command usage within the Sublayer CLI. This improves user experience by clearly showing which command corresponds to each action.

The `banner` method is beneficial in several ways:
- **User Experience**: Provides clarity for users trying to understand command functionalities and names.
- **Enhanced Documentation**: Simplifies the process of discovering functionalities via `thor --help` by explicitly connecting the banner text to specific actions.

## Try making your own Action:

{% @iframe/iframe url="https://blueprints.sublayer.com/interactive-code-generator/sublayer-actions" %}

## Examples:

- [WriteFileAction](https://github.com/sublayerapp/tddbot/blob/43297c5da9445bd6c8882d5e3876cff5fc6b2650/lib/tddbot/sublayer/actions/write_file_action.rb): Writes text to a specified file.
- [RunTestCommandAction](https://github.com/sublayerapp/tddbot/blob/43297c5da9445bd6c8882d5e3876cff5fc6b2650/lib/tddbot/sublayer/actions/run_test_command_action.rb): Runs a test command on the command line returning the output.
- [SpeechToTextAction](https://github.com/sublayerapp/rails_llm_voice_chat_example/blob/93300f268dde359b58c92a60db4b54d128d9d965/lib/sublayer/actions/speech_to_text_action.rb): Makes an API call to OpenAI's SpeechToText endpoint with audio data and returns text.
- [TextToSpeechAction](https://github.com/sublayerapp/rails_llm_voice_chat_example/blob/93300f268dde359b58c92a60db4b54d128d9d965/lib/sublayer/actions/text_to_speech_action.rb): Makes an API call to OpenAI's Speech Synthesis endpoint with text and returns audio data.