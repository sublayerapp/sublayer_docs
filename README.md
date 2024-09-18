## A model-agnostic AI Agent framework for Ruby

Combine Generators, Actions, Tasks, and Agents to build AI-powered applications!

- [Get Started](/docs/quick_start.md)
- [View on Github](https://github.com/sublayerapp/sublayer)

## Quick Links

Sublayer is a self-assembling, model-agnostic, AI Agent framework in Ruby that allows you to effortlessly create generative AI-powered automations.

- [Quick Start](/docs/quick_start.md): Get started with Sublayer right away.
- [Examples](/docs/guides/overview.md): Browse example code showing how you can use the Sublayer gem.
- [Framework Guide](/docs/concepts/overview.md): Learn about Sublayer concepts and conventions.
- [Advanced Config](/docs/advanced_config.md): Step-by-step guides to setting up your system and installing the library.

## New Features

### Banner Method for Thor Commands

As of the latest update, we've added a `banner` method to the Thor command-line interface classes in Sublayer, which affects the output of the `thor --help` command. This enhancement provides clear command name displays for sublayer generators, actions, agents, and projects, improving user experience and usability.

#### Examples

When you run `thor --help`, you'll now see specific command names listed:

- `sublayer generate:action`
- `sublayer generate:agent`
- `sublayer generate:generator`
- `sublayer new PROJECT_NAME`

### Purpose

The `banner` method customizes how command names are displayed, making it easier to identify and understand the functionality of each component at a glance. It's particularly useful for developers who want to quickly navigate the available commands when building AI-powered applications with Sublayer.

### Benefits

Implementing the `banner` method improves user experience by organizing and clarifying the commands. It aids in efficient project setup and management, especially for those new to using Thor or working with Sublayer tools.

### Usage

If you are developing with Thor and want to implement similar features in your CLI tools, this version of Sublayer can serve as a reference point for adding `banner` methods.

---

Ensure that the updated `README.md` provides users with detailed instructions and contextual understanding of the benefits introduced in the latest update, alongside guidance on maximizing the functionality of the Sublayer framework.
