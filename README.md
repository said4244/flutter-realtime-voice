# Browser Voice Chat with WebRTC

I built this proof of concept to try a spoken Arabic conversation directly in the browser. An Express backend requests a temporary OpenAI session credential, and the browser uses it to establish the realtime WebRTC connection.

**Built with:** JavaScript, HTML, CSS, Node.js, Express, WebRTC, OpenAI.

## What it does

- Start a microphone-based conversation from a browser UI.
- Request a temporary session credential through the backend.
- Send realtime events over a WebRTC data channel.
- Display session activity and conversation controls.

## Run locally

Install Node.js 18 or newer. Copy `.env.example` to `.env` and set `OPENAI_API_KEY`.

```bash
npm install
npm start
```

Open `http://localhost:3000` and allow microphone access. The provider key stays
in the Node process; `/session` returns the temporary session information.

Run `npm run check` to check the JavaScript syntax.

## Project layout

| Path | Purpose |
| --- | --- |
| `client/index.html` | Browser interface |
| `client/script.js` | Microphone, WebRTC, and session events |
| `client/style.css` | Page styling |
| `server/server.js` | Static hosting and session broker |
| `package.json` | Dependencies and run commands |
