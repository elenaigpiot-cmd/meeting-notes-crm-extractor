# Meeting Notes → CRM Action Extractor
> Built with n8n + Claude API (Anthropic) · Enterprise workflow automation

**[▶ Watch the 90-second demo](#)** ← *(to add Loom link here after recording)* !!!

---

## The problem
After every sales call, someone has to manually read through the transcript and figure out: who said they'd do what, where is this deal, what are the concerns. It takes 15-20 minutes per call and things get missed.

## What it does
Paste in a raw meeting transcript → Claude extracts structured data → Google Sheets logs it automatically.

**Output per transcript:**
- ✅ Deal name and stage
- ✅ Next steps with owner and due date
- ✅ Client concerns and objections
- ✅ Ready-to-paste CRM note

## Demo

**Input** — raw transcript:
> "Call with Acme Corp, May 24th. John said they love the demo but are concerned about GDPR compliance. Lisa mentioned budget is approved but needs CTO sign-off. Sarah to send security whitepaper by Friday..."

**Output** — auto-logged to Google Sheets:

| Date | Deal Name | Deal Stage | Next Steps | CRM Note |
|------|-----------|------------|------------|----------|
| 2026-05-24 | Acme Corp | Proposal sent | Send security whitepaper (Sarah), Obtain CTO sign-off (Lisa) | Met with John and Lisa at Acme Corp. Client expressed strong interest but raised GDPR concerns. CTO sign-off required before deal can proceed. |

## Architecture
