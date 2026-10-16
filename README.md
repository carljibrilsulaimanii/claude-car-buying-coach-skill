# Car Buying Coach: a Claude skill built from TikTok videos

A Claude skill that coaches you through buying or leasing a car and drafts the
texts and emails you send dealerships. It was built by downloading about 1,400
videos from a former dealership salesperson and finance manager, transcribing
them locally, and distilling the method into a skill.

## What's in here

| Path | What it is |
|---|---|
| `skill/car-buying-coach/` | The skill source: `SKILL.md` plus topic references |
| `car-buying-coach.skill` | The same skill zipped, ready to upload to claude.ai |
| `pipeline/` | How it was built: yt-dlp download, faster-whisper transcription, distilling |

## Install the skill

**claude.ai (also shows up in the Claude phone app)**

1. Go to claude.ai → **Settings** → **Capabilities**.
2. Under **Skills**, click **Upload skill**.
3. Pick `car-buying-coach.skill` from this repo.
4. Turn it on. It's now available on the web, desktop and mobile apps under
   the same account.

**Claude Code**

Copy the folder into your personal skills directory:

```powershell
Copy-Item -Recurse skill\car-buying-coach "$env:USERPROFILE\.claude\skills\"
```

## Using it

Just talk about the car you're buying. It triggers on things like:

- "I'm looking at a RAV4, where do I start?"
- "The dealer quoted me $48k out the door. Is that good?"
- "They're charging $2,000 for a protection package."
- "Help me reply to this salesperson."

It works one decision at a time and writes the actual messages to send.

## Rebuilding it or making your own

See [`pipeline/README.md`](pipeline/README.md). The same steps work for any
creator whose videos teach a repeatable method.

## Notes

- Consumer education, not financial or legal advice. Rates, rebates and state
  rules change, so treat dollar figures as rules of thumb.
- The source videos and transcripts are not included. They belong to their
  creator.

Built by Jibril Sulaiman.
