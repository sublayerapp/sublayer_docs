## Set Up Your Preferred LLM

After installing Sublayer, you can choose between any of the available LLM providers we support. This section will guide you through setting up and using these models, ensuring that you are up-to-date with the latest configurations and options.

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

### Setting Up Custom Providers

You can extend the functionality of the Sublayer LLM integration by creating custom providers. This section gives an overview of creating these providers based on examples such as OpenAI, Claude, and Gemini.

```ruby
module Sublayer
  module Providers
    class CustomProvider
      def self.call(prompt:, output_adapter:)
        # Add your custom implementation here
      end
    end
  end
end
```

### Consistent Model Versioning

To ensure that all references to LLM model versions across the documentation are consistent with the updated configurations, always specify the exact model names and versions as defined in the YAML configurations.

### Nous Research (Running locally)

Follow our [local model set up instructions](/docs/guides/running-local-models-with-llamafile.md)

Usage:

```ruby
Sublayer.configuration.ai_provider = Sublayer::Providers::Local
Sublayer.configuration.ai_model = "LLaMA_CPP"
```