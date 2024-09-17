## Set Up Your Preferred LLM

After installing Sublayer, you can choose between any of the available LLM providers we support.

### OpenAI (Default)

Set your `OPENAI_API_KEY` environment variable. (Visit [OpenAI](https://openai.com/product) to get an API key.)

Usage:

```ruby
Sublayer.configuration.ai_provider = Sublayer::Providers::OpenAI
Sublayer.configuration.ai_model = "gpt-4-turbo-preview"
```

### Anthropic

Supported Models: Claude 3 Opus, Claude 3 Haiku, Claude 3 Sonnet

Set your `ANTHROPIC_API_KEY` environment variable. (Visit [Anthropic](https://anthropic.com/) to get an API key.)

Usage:

```ruby
Sublayer.configuration.ai_provider = Sublayer::Providers::Claude
Sublayer.configuration.ai_model = "claude-3-opus-20240229"
```

### Google

Set your `GEMINI_API_KEY` environment variable. (Visit [Google AI Studio](https://ai.google.dev/) to get an API key.)

Usage:

```ruby
Sublayer.configuration.ai_provider = Sublayer::Providers::Gemini
Sublayer.configuration.ai_model = "gemini-pro"
```

### Groq

Set your `GROQ_API_KEY` environment variable. (Visit [Groq](https://console.groq.com/) to get an API key.)

Usage:

```ruby
Sublayer.configuration.ai_provider = Sublayer::Providers::Groq
Sublayer.configuration.ai_model = "mixtral-8x7b-32768"
```

### Nous Research (Running locally)

Follow our [local model set up instructions](/docs/guides/running-local-models-with-llamafile.md)

Usage:

```ruby
Sublayer.configuration.ai_provider = Sublayer::Providers::Local
Sublayer.configuration.ai_model = "LLaMA_CPP"
```

### Using the Sublayer Generate Agent Command

The `sublayer generate agent` command is a versatile tool that allows you to create new Sublayer Agents based on specific descriptions and operational parameters. To use this command, you should specify the necessary options such as description, provider, and model.

Here's an example of how to set up and use the command:

```bash
sublayer generate agent \
  --description "A Slack notification agent for error logging" \
  --provider OpenAI \
  --model "gpt-4o"
```

#### Options Available

- **Description**: Specifies the purpose and goal of the agent you're generating.
- **Provider**: The AI provider (e.g., OpenAI, Claude, Google) that you want to use.
- **Model**: The specific AI model to utilize, such as "gpt-4o" or "claude-3-haiku-20240307".

When using this command, make sure your environment variables for the selected provider are properly set to avoid any authentication issues.

By integrating this command into your workflow, you can quickly deploy AI-driven agents capable of performing complex tasks and automations.