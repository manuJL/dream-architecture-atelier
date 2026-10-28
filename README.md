# Dream Architecture Atelier

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)

> Transform personal dreams and nightmares into precise architectural spaces using a multi-agent system in Google AI Studio.

**Dream Architecture Atelier** is a lightweight, multi-agent pipeline for [Google AI Studio](https://aistudio.google.com) that turns raw dream descriptions into detailed architectural reconstructions and cinematic image prompts ready for AI image models.

## What is this?

Dreams twist space, break physics, and evoke powerful emotions. This project treats those constraints as design rules. By extracting the feeling, senses, and logic of a dream, it reconstructs it as if it were a real structure, then translates that reconstruction into a clean, high-quality prompt for image generation.

## The Four Agents

| Agent | Role | Function |
| :-- | :-- | :-- |
| **Extractor Agent** | Breaks the dream down into emotions, spaces, sensory details, physical rules, and symbolic objects. | `extract_dream_elements` |
| **Architect Agent** | Reconstructs those elements into a precise architectural space, defining form, materials, lighting, gravity/physics, movement, and emotional temperature. | `reconstruct_architecture` |
| **Image Prompt Agent** | Translates the architectural reconstruction into a powerful, cinematic image generation prompt. | `generate_image_prompt` |
| **Refine Agent** | Triggered on user request to iterate on the space, mood, or prompt without restarting from scratch. | `refine_architecture` |

**Default flow:** `Your Dream → Extractor → Architect → Image Prompt → Clean Final Summary`  
*The Refine Agent can be used at any time for changes.*

## How to Use in Google AI Studio

1. **Go to Google AI Studio** – Open [aistudio.google.com](https://aistudio.google.com).
2. **Create a new chat prompt** – Start a new "Chat prompt".
3. **Add the system instruction** – Copy the entire contents of [`system-instruction.txt`](./system-instruction.txt) into the **System Instructions** field.
4. **Enable Function Calling** – Go to *Tools > Function calling* and import all four JSON schemas from the [`functions/`](./functions/) folder.
5. **Describe your dream** – Paste your dream description into the chat, or use [`examples/sample-dream.md`](./examples/sample-dream.md) to test.
6. **Refine as needed** – If you'd like to tweak anything, just ask and the Refine Agent will handle it.

For a more detailed walkthrough, check out the [Setup Guide](./docs/setup-guide.md).

## Example: Input → Output

### Input

See [`examples/sample-dream.md`](./examples/sample-dream.md)

### Output

See [`examples/sample-output.md`](./examples/sample-output.md) for a full breakdown from all four agents, including the final cinematic image prompt.

## Features

- **Multi-agent workflow** – Clear separation of responsibilities for consistent results
- **Google Gemini Function Calling** – Structured, reliable outputs
- **Architectural reconstruction** – Goes beyond description to treat dreams as built spaces
- **Cinematic image prompts** – Optimized for Gemini, Midjourney, GPT-Image, Flux, Ideogram, and more
- **Iterative refinement** – Adjust mood, form, or lighting without redoing everything
- **Minimal & portable** – Just a system prompt + JSON schemas, no heavy code required

## Project Structure

```text
dream-architecture-atelier/
├── README.md
├── LICENSE
├── system-instruction.txt
├── functions/
│   ├── extract_dream_elements.json
│   ├── reconstruct_architecture.json
│   ├── generate_image_prompt.json
│   └── refine_architecture.json
├── examples/
│   ├── sample-dream.md
│   └── sample-output.md
└── docs/
    └── setup-guide.md
```

## License

This project is licensed under the [MIT License](./LICENSE).
