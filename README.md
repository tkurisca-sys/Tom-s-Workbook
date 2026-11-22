# Seedling

Seedling is an educational prototype that helps beginners understand startup valuations. You pick a fictional startup, read a research guide that shows how an AI could help you size up a business, and calculate what a hypothetical investment would mean in ownership.

**Intended user:** Beginners who want to understand startup valuations and learn what questions to ask before treating a business pitch as investment evidence.

**Problem:** Startup pitches and ownership percentages are hard to read when you're new. Seedling shows the basic ownership math and points out what's uncertain and what evidence is missing, without anyone investing real money.

> All companies, valuations, and comparison data in Seedling are fictional. This is not investment advice and not an offer to invest.

---

## Links

- **Live prototype:** https://seedling-startup-investing-demo.replit.app
- **Access:** No login, invite code, or account needed. Just open the link.

## Demo Video

- **Draft demo (Google Drive):** [[https://drive.google.com/drive/u/2/folders/1A7vPQWASUvGrOovrIM-c6vFZm21T2Jtr]
- Viewing access is granted to Emelia Hughes and Samuel Huang.

---

## Where to Find Everything

| Component | Location |
|---|---|
| Prototype code (the live app) | [`artifacts/seedling/index.html`](artifacts/seedling/index.html) |
| Assets (favicon, robots.txt) | [`artifacts/seedling/public/`](artifacts/seedling/public/) |
| Revision documentation (priorities, peer feedback, tests, before and after, risk response) | [`artifacts/seedling/docs/revision.md`](artifacts/seedling/docs/revision.md) |
| AI-use disclosure (draft) | [`artifacts/seedling/docs/ai-use-disclosure.md`](artifacts/seedling/docs/ai-use-disclosure.md) |
| Demo notes and recording outline | [`artifacts/seedling/docs/demo-notes.md`](artifacts/seedling/docs/demo-notes.md) |
| Automated logic tests | [`artifacts/seedling/tests/`](artifacts/seedling/tests/) |
| Feature details and limitations | [`artifacts/seedling/README.md`](artifacts/seedling/README.md) |

**Note on the code:** The whole Seedling app lives in `artifacts/seedling/index.html`. The files in `artifacts/seedling/src/` are unused starter code from Replit and are not part of the live page. The `api-server`, `lib/`, and `mockup-sandbox` folders are workspace scaffolding and are not used by the app.

---

## How to Use It

1. Open the live prototype.
2. Pick one of three fictional startups:
   - **Canopy:** $4,000,000 example valuation
   - **Orbit Pantry:** $2,500,000 example valuation
   - **Tidewell:** $6,000,000 example valuation
3. Read the research guide. It shows what the business does, two key uncertainties, two questions to investigate, and what evidence is missing.
4. Enter a hypothetical dollar amount and click **Calculate example ownership**.
5. The result shows your example ownership percentage with a reminder that it's only an illustration.
6. Click **Start over** to clear everything and try another startup.

**How the result is calculated:**

`Example ownership = amount ÷ example valuation × 100`

For example, $1,000 in Canopy ($4,000,000) = **0.0250%** ownership.

**Optional:** Below the calculator, you can enter a city or region and toggle Local, National, and Global tables that compare fictional businesses by reach. This section doesn't change the ownership calculation.

---

## AI Role

**What the AI is meant to do:** Help a beginner understand a startup pitch by pointing out uncertainties, questions to research, and missing evidence. It gives a plain-language research guide, not a buy or sell recommendation.

**Intended input:** A startup pitch and supporting company information.
**Intended output:** A research guide with uncertainties, questions, and missing evidence.

**Current status:** This prototype uses **Wizard-of-Oz prototyping**. No AI model runs in the app. The research guides are prepared text written ahead of time to show what the AI experience would look like.

| Feature | Status | How it works now |
|---|---|---|
| Startup research guide | Simulated | Prepared text pulled up when you pick a startup |
| Key uncertainties | Simulated | Fixed list for each startup |
| Questions to investigate | Simulated | Fixed list for each startup |
| Missing evidence | Simulated | Fixed text for each startup |
| Analysis of a user's own pitch | Planned | Not built yet |
| Finding and checking sources | Planned | Not built yet |
| Ownership calculator | Working (not AI) | Basic math |
| Local area filter and tables | Working (not AI) | Text matching on fictional data |

The app labels this clearly with a **"Simulated · not live AI"** tag on the research guide.

---

## What Changed in This Revision

Based on peer feedback and my own testing, I focused on three improvements to the central task:

1. **Made the AI guide more useful.** The first version was a short snapshot. It's now a structured guide with what the business does, uncertainties, research questions, and missing evidence.
2. **Explained the comparison tables.** Peer feedback said the geographic checkboxes were confusing. The section now explains its purpose and states the data is fictional.
3. **Blocked impossible results.** Before, entering $5,000,000 for Canopy showed 125% ownership. Now the app stops the calculation and explains the $4,000,000 limit. Old results also hide when you change your input, so you never see a stale number.

Full details, the peer feedback table, the five test cases, and the before and after comparison are in [`revision.md`](artifacts/seedling/docs/revision.md).

---

## Risk Response

**Risk:** Over-reliance on AI. A beginner could treat the AI guide or ownership number as real investment evidence.

**What I changed:**
- Every guide ends with a "missing evidence" note explaining what's not proven, like audited financials or customer contracts.
- The guide is labeled as simulated, and the app states no facts are verified.
- Ownership is capped at 100%, so the app can't show an impossible result.
- The result panel reminds you it's an illustration and no real money is invested.

**What risk remains:** The guides are fixed text, so users can't edit, reject, or regenerate them. The math also ignores dilution, fees, and share classes. A real version would need a way to check sources and push back on the AI's output.

More in [`revision.md`](artifacts/seedling/docs/revision.md).

---

## Known Limitations

- Research guides are prepared text, not generated or verified analysis.
- I don't have evidence yet that the revised guides help real users.
- All valuations, companies, and comparison data are fictional.
- The formula ignores dilution, fees, share classes, and legal terms.
- Very small amounts can round to $0.00 or 0.0000%.
- Local area matching only knows three demo regions (New York City region, San Francisco Bay Area, Greater London) and resets when you reload.
- "Start over" doesn't reset the comparison tables.
- Tests check the logic but not full browser, keyboard, or screen reader behavior.

## Next Priorities

1. Test the research guide with real beginners to see if it actually helps them ask better questions.
2. Let users edit, reject, or ask follow-up questions about the guide.
3. Connect a live AI model that can read a user's own pitch, and test its accuracy.

---

## AI-Use Disclosure

Read it here: [`ai-use-disclosure.md`](artifacts/seedling/docs/ai-use-disclosure.md)

---

## Privacy and Data

- Seedling doesn't save anything you enter. Your startup choice, amount, and local area stay in the page and are gone when you leave.
- No accounts, cookies, or databases are used by the app.
- No API keys, passwords, or tokens are stored in this repo.

## Running It

The easiest way is the live link above. To run it yourself, open the project in Replit and click **Run**.# Tom-s-Workbook
AGENTIC AI ESTEEM class
