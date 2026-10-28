# Dream Architecture Atelier

A multi-agent system for Google AI Studio that transforms personal dreams and nightmares into precise architectural spaces.

## What it does

1. **Extractor Agent** → Breaks down the dream into emotions, spaces, sensory details, and physical rules
2. **Architect Agent** → Reconstructs the dream as architecture (materials, lighting, gravity, emotional temperature)
3. **Image Prompt Agent** → Creates a cinematic image generation prompt
4. **Refine Agent** → Allows iterative improvement

## How to use in Google AI Studio

1. Go to [Google AI Studio](https://aistudio.google.com)
2. Create a new prompt
3. Paste the content of `system-instruction.txt` into the **System Instruction**
4. Add the four functions from the `functions/` folder
5. Describe your dream in the chat

## Features

- Multi-agent workflow
- Function calling
- Structured extraction
- Cinematic image prompt generation
- Iterative refinement

## License

MIT
