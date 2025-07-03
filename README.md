# Fragments 

An open-source platform inspired by Anthropic's Claude Artifacts, Vercel v0, and GPT Engineer, powered by the **E2B SDK**.

## Overview

Fragments is a versatile AI-powered code generation and execution platform built on modern web technologies. It enables secure, streaming execution of AI-generated code across multiple supported stacks and LLM providers, all within a user-friendly interface.

## Features

- Built with **Next.js 14** (App Router, Server Actions), **shadcn/ui**, **TailwindCSS**, and **Vercel AI SDK**.
- Uses the **E2B SDK** to securely execute AI-generated code in isolated sandboxes.
- Real-time streaming output in the UI.
- Supports installing and using any npm or pip packages dynamically.
- Multiple supported development stacks (expandable):
  - Python interpreter
  - Next.js
  - Vue.js
  - Streamlit
  - Gradio
- Compatible with a wide range of LLM providers (expandable):
  - OpenAI
  - Anthropic
  - Google AI
  - Mistral
  - Groq
  - Fireworks
  - Together AI
  - Ollama

## Getting Started

### Prerequisites

- Git
- Recent Node.js and npm versions
- E2B API Key
- API key for your chosen LLM provider(s)

### Installation

Clone the repository:

```bash
git clone https://github.com/e2b-dev/fragments.git
cd fragments
```

Install dependencies:

```bash
npm install
```

### Configuration

Create a `.env.local` file in the root directory and add your API keys:

```env
E2B_API_KEY="your-e2b-api-key"
OPENAI_API_KEY="your-openai-api-key"
# Add other provider keys as needed:
ANTHROPIC_API_KEY=
GROQ_API_KEY=
FIREWORKS_API_KEY=
TOGETHER_API_KEY=
GOOGLE_AI_API_KEY=
GOOGLE_VERTEX_CREDENTIALS=
MISTRAL_API_KEY=
XAI_API_KEY=
```

You can also configure optional environment variables for domain, rate limiting, analytics, and more as needed.

### Running the Development Server

Start the app locally:

```bash
npm run dev
```

### Building for Production

Build the app:

```bash
npm run build
```

## Customization

### Adding Custom Personas and Templates

- Install and log in with the E2B CLI.
- Add new sandbox templates under `sandbox-templates/`.
- Initialize templates using `e2b template init`.
- Customize the `e2b.Dockerfile` and `e2b.toml` to define dependencies and start commands.
- Build templates with `e2b template build --name `.
- Register your templates in `lib/templates.json`.

### Adding Custom LLM Models and Providers

- Add new models in `lib/models.json`.
- Define new providers in `lib/models.ts` with appropriate API configurations.
- Add logos for new models/providers under `public/thirdparty/logos`.

## Contributing

Contributions are welcome! Please open issues or pull requests to report bugs, suggest features, or improve documentation.

## License

This project is open source under the MIT License.

