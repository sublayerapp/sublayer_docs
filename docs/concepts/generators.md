# Generators

Generators are responsible for generating specific outputs based on input data. They focus on a single generation task and do not perform any actions or complex decision-making. Generators are the building blocks of the Sublayer framework.

### Banner Method

In each generator class, a `banner` method can be added to define the command name that is displayed when running the `thor --help` command. This method improves the user experience by providing a clear, specific name for the command-line generator, enhancing usability and clarity.

#### Example

Suppose you have a generator named `MyGenerator`. You can declare a `banner` method to customize the command name display:

```ruby
class MyGenerator < Sublayer::Generators::Base
  def self.banner
    "sublayer generate:my_generator"
  end

  # ... rest of the generator code
end
```

When running `thor --help`, the command name will now appear as `sublayer generate:my_generator`, clearly indicating its purpose and use.

### Benefits of Using the Banner Method

- **Clarity:** Clearly specifies the command's functionality.
- **Customization:** Allows developers to define how commands appear in help menus.
- **User Experience:** Enhances user understanding and navigation in CLI tools.

### Try making your own generator:

{% @iframe/iframe url="https://blueprints.sublayer.com/interactive-code-generator/sublayer-generators?example=true" %}

### [Examples](https://github.com/sublayerapp/sublayer/tree/main/examples):

* [CodeFromDescriptionGenerator](https://github.com/sublayerapp/sublayer/blob/main/examples/code\_from\_description\_generator.rb): Generates code based on a description and the technologies used.
* [DescriptionFromCodeGenerator](https://github.com/sublayerapp/sublayer/blob/main/examples/description\_from\_code\_generator.rb): Generates a description of the code passed in to it.
* [CodeFromBlueprintGenerator](https://github.com/sublayerapp/sublayer/blob/main/examples/code\_from\_blueprint\_generator.rb): Generates code based on a blueprint, a blueprint description, and a description of the desired code.