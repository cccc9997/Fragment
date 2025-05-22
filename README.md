
# Fragments

Fragments is an open-source platform inspired by apps like Anthropic's Claude Artifacts, Vercel v0, and GPT Engineer. It enables you to build, run, and interact with AI-generated code in secure sandboxes, supporting multiple programming stacks and LLM providers.

Powered by the [E2B SDK](https://e2b.dev/).

---

## Features

- ⚡️ **Modern stack:** Next.js 14 (App Router, Server Actions), shadcn/ui, TailwindCSS, Vercel AI SDK  
- 🔒 **Secure code execution:** Uses E2B SDK to safely run AI-generated code  
- 💻 **Streaming UI:** Real-time output streaming in the browser  
- 📦 **Flexible environments:** Install and use any package from npm or pip  
- 🧑‍💻 **Supported stacks:**  
  - Python interpreter
  - Next.js
  - Vue.js
  - Streamlit
  - Gradio
- 🤖 **Supported LLM providers:**  
  - OpenAI
  - Anthropic
  - Google AI
  - Mistral
  - Groq
  - Fireworks
  - Together AI
  - Ollama

---

## Getting Started

### Prerequisites

- [git](https://git-scm.com/)
- Recent version of [Node.js](https://nodejs.org/) and npm
- [E2B API Key](https://e2b.dev/)
- API key for your preferred LLM provider (OpenAI, Anthropic, etc.)

### 1. Clone the Repository

```bash
git clone https://github.com/cccc9997/Fragment.git
cd Fragment
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Set Environment Variables

Create a `.env.local` file in the root directory and set your API keys:

```env
E2B_API_KEY=your-e2b-api-key
OPENAI_API_KEY=your-openai-api-key
# Add additional provider keys as needed:
# ANTHROPIC_API_KEY=
# GROQ_API_KEY=
# FIREWORKS_API_KEY=
# TOGETHER_API_KEY=
# GOOGLE_AI_API_KEY=
# MISTRAL_API_KEY=
```
See the repository for more optional environment variables (analytics, rate limiting, etc.).

### 4. Start the Development Server

```bash
npm run dev
```

Visit [http://localhost:3000](http://localhost:3000) to use the app.

### 5. Build for Production

```bash
npm run build
```

---

## Customization

### Adding Custom Personas (Sandbox Templates)

1. Install and log in to the [E2B CLI](https://e2b.dev/docs/cli).
2. Add a new folder under `sandbox-templates/`.
3. Initialize a new template:
   ```bash
   e2b template init
   ```
4. Edit the generated `e2b.Dockerfile` and `e2b.toml` to define your environment and start command.
5. Build and deploy the template:
   ```bash
   e2b template build --name 
   ```
6. Add the template to `lib/templates.json` with its metadata.

### Adding Custom LLM Models or Providers

- Add new models to `lib/models.json`.
- Add new providers to `lib/models.ts` in the `providerConfigs` list.

---

## Contributing

We welcome contributions! Please open an issue or submit a pull request for bug fixes, improvements, or new features.

---

## License

MIT

