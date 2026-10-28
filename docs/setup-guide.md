# Setup Guide

## Step-by-step in Google AI Studio

1. **Open Google AI Studio** – Go to [Google AI Studio](https://aistudio.google.com).
2. **Create a prompt** – Create a new **Chat prompt**.
3. **Select a model** – Gemini 2.5 Pro or Gemini 2.5 Flash is recommended.
4. **Add System Instructions** – Copy the entire contents of [`system-instruction.txt`](../system-instruction.txt) and paste it into the **System Instructions** field.
5. **Enable Function Calling** – Go to *Tools > Function calling*.
6. **Import the functions** – Add all four JSON files from the [`functions/`](../functions/) folder (`extract_dream_elements.json`, `reconstruct_architecture.json`, `generate_image_prompt.json`, `refine_architecture.json`).
7. **Test it out** – Paste your dream description, or copy the contents of [`examples/sample-dream.md`](../examples/sample-dream.md) into the chat and run it.
8. **Refine** – Want changes? Just describe them and the Refine Agent will take over.
