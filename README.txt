LITTLE BEINGS V5 — REAL AI CHAT

What changed: The original V4.5 creature game has been upgraded with a secure AI chat backend. The UI, creatures, animations, actions, and local memory remain.

TEST THE GAME OFFLINE:
Open index.html in Chrome. Selection, naming, Feed/Play/Rest and saved memories should work. Chat requires Netlify deployment and an API key; it will show a clear connection message offline.

ENABLE REAL AI CHAT:
1. Get a Gemini API key from https://aistudio.google.com/apikey (check Google's terms and pricing).
2. Log in to https://app.netlify.com and create a new site.
3. Upload/deploy this entire folder as a project, including netlify/functions/chat.js and netlify.toml. For reliable function builds, use a Git repository connected to Netlify rather than a static HTML-only file drop.
4. In Netlify project configuration -> Environment variables, add GEMINI_API_KEY with your key. Scope it to Functions. NEVER put it in index.html or public JavaScript.
5. Trigger a fresh deploy. Open your Netlify URL. Chat status should say Real AI ready.

NOTES:
- Public AI calls may cost money and can be abused. Before public launch, add abuse controls: rate limits, per-user quotas, captcha or account login, plus budgets/alerts.
- Conversation and memory are currently stored in the browser only, not synchronized between devices. Recent 26 messages + saved facts are passed to AI on each turn, so this is not unlimited long-term memory.
- The AI can be wrong; its responses are model-generated, not verified facts.
- Do not put personal secrets into the demo.
- If you only double-click HTML, the game works but it cannot access the server-side AI function.
