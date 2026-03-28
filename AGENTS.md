# AGENTS.md

## Cursor Cloud specific instructions

### Overview

This is a single-file client-side web application (`trial-companion-app.html`) — a Voice ePRO (electronic Patient-Reported Outcomes) agent for clinical trials called **Trial Companion**. There is no build system, no package manager, no backend, and no database.

### Running the app

Serve the HTML file over HTTP (required because the app uses ES modules with `type="module"`):

```
python3 -m http.server 8080
```

Then open `http://localhost:8080/trial-companion-app.html` in a browser.

### Modes

- **Demo Mode**: Click "Run Demo Mode" on the setup screen. No external API keys needed. Use the yellow strip buttons ("Simulate Session Complete", "Trigger Safety Alert") to exercise all features.
- **Live Mode**: Requires an ElevenLabs Agent ID. The app loads the ElevenLabs Conversational AI SDK at runtime from `https://esm.sh/@11labs/client`.

### Lint / Test / Build

There are no lint, test, or build steps — this is a single HTML file with inline CSS and JS. Validate by serving and opening in a browser.
