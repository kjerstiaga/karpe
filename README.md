# 🎵 Suno v5.5 Lyrics + Prompt Generator

An AI-powered tool that generates complete song lyrics and Suno v5.5 style prompts based on your music idea — built with React and the Anthropic Claude API.

## What it does

Give it a concept, mood, and genre reference — it outputs:

- **Full lyrics** with Suno-ready structure tags (`[Intro]`, `[Verse 1]`, `[Chorus]`, `[Bridge]`, etc.)
- **A Suno v5.5 style prompt** layered with genre, instrumentation, vocal character, texture, and emotional arc

## Getting started

The app runs as a single file. Rename or use it as `index.html` if converting to plain HTML, or deploy the `.jsx` file via any React-compatible environment (Vite, CodeSandbox, Claude Artifacts, etc.).

### Prerequisites

- An [Anthropic API key](https://console.anthropic.com/) — the app calls `claude-sonnet-4-20250514` via `/v1/messages`
- The API key must be injected at the proxy/environment level (the app does not take a key field directly)

### Run locally with Vite

```bash
npm create vite@latest suno-generator -- --template react
cd suno-generator
# Replace src/App.jsx with the contents of index.html / suno-karpe.jsx
npm install
npm run dev
```

## Usage

1. Fill in the five fields:
   - **Concept** — what the song is about
   - **Mood** — emotional tone
   - **Genre / reference artist** — style anchor
   - **Vocal tone** *(optional)*
   - **Lyrics language** *(optional, defaults to Norwegian)*

2. Click **Generer Lyrics + Suno-prompt**

3. Copy lyrics into Suno's lyrics field (tags intact), and the style prompt into Suno's style field

4. Generate 2–4 variants in Suno and pick the best one

## Tips

- Use **Section Regeneration** in Suno on weak parts rather than regenerating the full song
- The style prompt is written in conversational language optimized for Suno v5.5's style interpreter
- Norwegian and English lyrics are both supported — specify in the language field

## Tech stack

- React (hooks only, no external UI libraries)
- Anthropic Claude API (`claude-sonnet-4-20250514`)
- Google Fonts: Bebas Neue, DM Mono, Instrument Serif
- Zero dependencies beyond React itself

## License

MIT
