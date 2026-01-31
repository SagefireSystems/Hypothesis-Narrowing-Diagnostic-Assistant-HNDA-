# Hypothesis-Narrowing Diagnostic Assistant (HNDA)
**Decision-quality optimizer for high-uncertainty thinking.**  
HNDA helps you decide **what to think next** by clarifying assumptions, handling evidence with integrity, prioritizing risk asymmetry and irreversibility, and preserving reversibility—without giving final decisions, diagnoses, or irreversible recommendations.

> **Non-goal:** This is not a problem-solver, authority, or strategist choosing outcomes.  
> **Goal:** Improve decision quality under uncertainty.

---

## What it does
HNDA is a prompt framework (and optional wrapper tooling) that enforces:
- Explicit separation of **facts vs assumptions vs hypotheses vs speculation**
- A staged reasoning flow (operators) to prevent premature closure
- Risk-first thinking (irreversibility > probability)
- Clear “pause / hand-off” when authority is exceeded
- A mandatory four-part ending structure for strategy-style responses:
  1) Live Hypotheses  
  2) Discriminating Information Needed  
  3) Reversible Probes  
  4) Stop / Escalation Conditions  

---

## What it does *not* do
HNDA will not:
- Provide final answers, diagnoses, or “what you should do”
- Make irreversible commitments or recommendations
- Give legal advice or fiduciary financial advice
- “Take accountability” or act as an executive decision-maker

---

## Quickstart
### Option A — Use as a Custom GPT / system prompt
1. Copy the full prompt from [`prompts/system_prompt.md`](prompts/system_prompt.md).
2. Paste it into your system instructions (e.g., Custom GPT or your app’s system prompt field).
3. Start with:  
   - the situation  
   - constraints  
   - what you already know  
   - what’s at stake if wrong

### Option B — Use in an application
- Feed `prompts/system_prompt.md` as the **system** message.
- Put user context/questions in the **user** message.
- Keep conversation history to preserve the operator flow and output contract.

---

## Recommended usage patterns
HNDA works best when you provide:
- **Known facts** (and their sources if possible)
- Your **assumptions** (even if uncertain)
- The **decision horizon** (hours, weeks, months)
- The **irreversibility / downside** if wrong
- The **constraints** (budget, time, legal, reputational, relationship)

---

## Repository contents
- `prompts/system_prompt.md` — canonical prompt (versioned)
- `docs/operators.md` — how the operator state machine works
- `docs/output_contract.md` — the mandatory structure and when it triggers
- `prompts/example_sessions.md` — examples showing how HNDA responds

---

## Safety & scope notes
HNDA is a thinking aid, not professional advice.  
If you are dealing with high-stakes medical, legal, financial, or safety-critical matters, use role-appropriate professionals.

---

## Contributing
Contributions are welcome, especially:
- Additional example sessions (good and bad)
- Tests for “no final decision” compliance
- Improvements to operator triggers and failure modes

See [CONTRIBUTING.md](CONTRIBUTING.md).

---

## License
Choose a license that matches your intent:
- MIT for maximal reuse
- Apache-2.0 for explicit patent grant
- CC BY for prompt text (if you want attribution requirements)

See [LICENSE](LICENSE).
