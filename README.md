# ContextBridge Privacy Policy

**Last updated: August 9, 2026**

ContextBridge ("the extension") is a Chrome extension that helps you transfer conversation context and files between AI chat platforms (ChatGPT, Claude, Gemini, Grok, Perplexity). This policy explains exactly what data the extension touches, where it goes, and what it never does.

---

## What the extension reads

When you click **Export Context** on a supported AI chat page, the extension reads:

- The visible text of your conversation on that page (messages you and the AI exchanged)
- File names and, where accessible, file URLs attached to that conversation
- The page URL and title

The extension does **not** read your conversation automatically or in the background. It only reads page content when you click a button inside the ContextBridge panel.

---

## Where your data goes

**Conversation text** you choose to export is sent to the ContextBridge backend server over HTTPS, which forwards it to Groq's AI API to generate a compressed summary. This happens only when you click **Export Context** or **Summarize Files**.

**Files** you choose to capture are processed locally in your browser and, if you choose to transfer them, are temporarily held in your browser's local extension storage (not sent to any server) so they can be attached to a new conversation on another platform.

The extension does not send your data to any third party other than:
- The ContextBridge backend (for compression)
- Groq's API (called by the backend, not the extension directly)

---

## What is stored, and where

The extension uses `chrome.storage.local`, which keeps data only on your own device and is never synced to a Google account or any external server. This includes:

- Saved snapshots of past exported contexts (so you can reuse them later)
- Your backend URL preference, if you changed it in Settings
- Temporarily queued files during a transfer (auto-cleared after 5 minutes)

You can clear all stored data at any time by removing the extension or clearing its storage via `chrome://extensions`.

---

## What the extension never does

- It does not track your browsing activity outside of the five supported AI platforms.
- It does not collect analytics, advertising identifiers, or usage statistics.
- It does not sell or share your data with advertisers or data brokers.
- It does not store your conversation content on any server after a compression request completes — the backend processes the request and returns a result without retaining a copy.
- It does not require you to create an account or sign in.

---

## Permissions explained

| Permission | Why it's needed |
|---|---|
| `activeTab` / host permissions for AI sites | To read conversation content only on the page you're actively using |
| `scripting` | To inject the floating ContextBridge panel into supported AI pages |
| `storage` | To save your snapshots and settings locally on your device |
| `tabs` | To open a new tab when you choose to continue a conversation on another platform |
| `clipboardWrite` / `clipboardRead` | To copy the generated prompt to your clipboard when you click Copy |

---

## Changes to this policy

If this policy changes, the "Last updated" date above will be revised. Continued use of the extension after changes means you accept the updated policy.

---

## Contact

For questions about this policy or the extension's data handling, contact: **manasworks75@gmail.com**
