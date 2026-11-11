# Hi, I'm Arunkumar Rajendran

I'm an **AI engineer** based in Abu Dhabi, working on automation, workflows and AI agents. I build systems that answer from real documents, hand over to a person when they should, and report honestly when a result is weak.

## Projects

### [rathinam-gpt](https://github.com/arunguru94/rathinam-gpt): a college assistant on Telegram
Students and parents scan a QR code and ask questions about the college. Retrieval-augmented generation with the vector database running locally, so no cloud vector store is involved.
- **n8n + Claude + ChromaDB** in Docker, with a file watcher that re-indexes documents automatically when they change.
- **Guardrails in the prompt:** answers only from retrieved context, ignores prompt-injection attempts, never shares personal data, replies in English or Tamil.
- Batched embedding writes with an automatic smaller-batch retry when one fails.

`Python` `FastAPI` `ChromaDB` `n8n` `Docker` `Claude API`

### [baggage-damage-claim](https://github.com/arunguru94/baggage-damage-claim): self-serve claims prototype
A traveller reports damaged baggage, uploads photos, and gets an AI assessment without waiting for an agent. A prototype, not a production service.
- Scans the PDF417 barcode on a boarding pass to find the booking.
- Claude analyses the damage photo and returns structured JSON: damage class, confidence, authenticity rating and a recommended action.
- **Doubtful cases are never auto-approved:** uncertain damage or suspicious photos go to manual review. Every AI call is logged for audit.

`React 19` `TypeScript` `Vite` `Tailwind` `Google Apps Script` `Claude API`

### [ipl-player-value](https://github.com/arunguru94/ipl-player-value): player value and squad selection for the IPL
Ball-by-ball data for 1,243 matches (295,732 deliveries) turned into a player-impact measure, a next-season forecast, and a squad optimiser that follows the IPL rules and the auction purse.
- Impact is measured against the same phase of the innings and the same ground. Team totals correlate **0.75** with win rate across 166 team-seasons.
- **Reported as it came out:** the forecast ranks players at about 0.16 correlation, no better than a plain three-season average, and a player's past record at a ground does not predict his later record there. So that feature is left out, and the report says so.

`Python` `pandas` `scikit-learn` `SciPy`

## How I work

- **Test before claiming.** Walk-forward tests against simple baselines, and a written list of limits in the README.
- **Agents with boundaries.** Answers grounded in retrieved text, injection handling, and a person in the loop when the model is unsure.
- **Audit trails.** AI calls and decisions are logged so a reviewer can see what happened.

## Stack

Python, FastAPI, pandas, NumPy, SciPy, scikit-learn · Claude API, retrieval with ChromaDB, n8n · TypeScript, React, Vite, Tailwind · Docker, Google Apps Script

## Contact

[Website](https://arunkumarrajendran.com) · [LinkedIn](https://www.linkedin.com/in/arunkumarrajendran)
