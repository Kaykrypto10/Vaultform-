# Vaultform

**Forms that tell the truth.**

A decentralized form and feedback platform built on Walrus. Every response is stored permanently onchain — tamper-proof, verifiable, and owned entirely by the form creator. Sensitive fields are encrypted with Seal so only the creator's wallet can read private responses.

Built for Walrus Sessions: Tools Builder Activation — Season 2.

---

## What It Does

Vaultform lets anyone create a custom form, share it via link, and collect responses that live on Walrus forever. No server. No middleman. No one edits what was submitted.

- **Create forms** — name them, add fields, configure required/optional inputs, toggle Seal encryption per field, publish to Walrus
- **Share via link** — anyone with the link can respond, no wallet or account needed
- **Store on Walrus** — every submission becomes a permanent blob with a verifiable ID
- **Encrypt with Seal** — sensitive fields encrypted before leaving the browser, decryptable only by the creator's wallet
- **Admin dashboard** — wallet-gated, filter submissions, add notes, star and prioritize responses, export to CSV
- **Submission receipt** — every respondent gets a Walrus blob ID and timestamp they can verify on walruscan.io

---

## Field Types Supported

- Short Text
- Rich Text
- Dropdown
- Checkboxes
- Star Rating (1 to 5)
- Screenshot / Image Upload
- Video Upload
- URL Link
- Confirmation Checkbox

All fields can be toggled required or optional. Any field can be marked for Seal encryption.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Storage | Walrus Protocol (HTTP API) |
| Encryption | Seal (client-side, identity-based) |
| Network | Sui Mainnet |
| Frontend | Vanilla HTML, CSS, JavaScript |
| Deployment | Walrus Sites via Walgo |

---

## How It Works

### Creating a Form
1. Open Vaultform and click **Create Form**
2. Enter form name, description, and your Sui wallet address
3. Add fields using the field type grid
4. Toggle required/optional and Seal encryption per field
5. Click **Publish Form to Walrus**
6. Vaultform stores the form configuration as a Walrus blob and returns a shareable link

### Submitting a Response
1. Open the shared form link
2. Fill in all fields
3. Click **Submit Response**
4. Vaultform stores the submission as a Walrus blob
5. A Submission Receipt is shown with the blob ID, timestamp, and a verification link on walruscan.io

### Accessing the Admin Dashboard
1. Click **Dashboard** in the nav
2. Enter your Sui wallet address to verify access
3. View all submissions, filter, search, add notes, set priority, and export to CSV

---

## Why Walrus

Most form tools store responses on servers that can be shut down, edited, or compromised. Vaultform uses Walrus because:

- **Tamper-proof** — every blob has a unique cryptographic ID. If the data changes, the ID changes. The original submission is always provable.
- **Permanent** — data is spread across hundreds of independent nodes with no single point of failure.
- **Verifiable** — anyone can check a blob ID on walruscan.io and confirm exactly what was submitted.
- **Programmable** — Walrus is built on Sui, making storage composable with onchain logic and access control.

This is not a Web2 form tool with a blockchain badge. The permanence and verifiability of Walrus is the product.

---

## Why Seal

Sensitive form fields are encrypted using Seal before being stored on Walrus. This means:

- Encrypted data is stored as a Seal-wrapped blob
- Only the form creator's wallet identity can decrypt responses
- Even if someone finds the blob ID, they see encrypted data they cannot read
- The admin dashboard decrypts automatically when the correct wallet is verified

---

## Live Demo

**Site:** https://degodman.wal.app

---

## Project Structure

```
vaultform/
└── index.html    # Complete single-file application
```

---

## Setup

No installation required. This is a single HTML file that runs entirely in the browser.

To run locally — open `index.html` in any modern browser.

To deploy on Walrus — upload `index.html` to Walgo at walgoweb.wal.app, connect a Sui wallet, and deploy to mainnet.

---

## Built By

**Godman** — Web3 Content Writer & Brand Strategist

- X: [@DeGodman10](https://x.com/DeGodman10)
- Telegram: @DeGodman11
- Email: kaykrypto10@gmail.com

---

## License

MIT
