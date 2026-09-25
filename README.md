# Pulse Data Rooms for Gemini CLI

Connect [Pulse](https://www.usepulse.co) to Gemini CLI. Ask about the documents in your data room, see who opened what you shared and for how long, and create share links, without leaving the terminal.

## Install

```bash
gemini extensions install https://github.com/usepulse-co/pulse-gemini-extension
```

The first time Gemini uses a Pulse tool, your browser opens a Pulse sign-in. Approve the connection and you are done. The connection is yours, not your company's, and you can revoke it any time in Pulse under Settings, Integrations.

Prefer to add the server yourself? `gemini mcp add --transport http pulse https://api.usepulse.co/mcp`

## What it can do

- Search the text of your documents and read any page
- See who opened your links, what they read, and how engaged each contact is
- Ask Perry, Pulse's analyst, a question and get a cited answer
- Create folders and share links, move and rename files, upload documents

Anything that deletes data or takes away access someone already has asks you to approve it first.

## Help

- Setup guide: https://www.usepulse.co/docs/mcp
- Privacy policy: https://www.usepulse.co/privacy-policy
- Support: support@usepulse.co

A Pulse account is required. Sign up at https://www.usepulse.co.
