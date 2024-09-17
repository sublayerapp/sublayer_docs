## Set Up Your Preferred LLM

After installing Sublayer, you can choose between any of the available LLM providers we support to power your agents and generators.

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

Set your `GOOGLE_API_KEY` environment variable. (Visit [Google AI Studio](https://ai.google.dev/) to get an API key.)

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

### Using Agents with LLM Providers

With the addition of the `sublayer generate agent` command, you can now create agents that leverage these LLM providers to perform tasks autonomously. Depending on the provider you select, make sure to have your API keys set correctly as described above to ensure seamless operation of your agents.