# House Prospects — Copilot Instructions

This repository contains Norwegian property sale prospects (prospekter) that we are evaluating for purchase.

## When a new PDF prospect is added

1. **Create a subfolder** named after the property address in kebab-case (e.g., `fredheimveien-9e/`)
2. **Move the PDF** into that subfolder
3. **Extract text** from the PDF using PyPDF2 (`pip install PyPDF2` if needed)
4. **Create `summary.md`** in the subfolder — translate all key information to English, structured as follows:
   - **Transit from Oslo S** (at the very top, before "At a Glance"): a table showing public transport route(s) from Oslo Central Station to the property, including mode (train/bus/tram), line numbers, and total travel time. Look this up via web search.
   - **At a Glance** table: asking price, shared debt, transaction costs, total price, monthly fees, usable area, bedrooms, bathrooms, ownership type, plot area, year built, energy rating, pre-emptive rights, pets policy
   - **Property Description**: layout by floor/plan, key features
   - **Location & Transport**: distances to schools, train stations, amenities
   - **Financial Details**: cost breakdown, shared debt terms (lender, interest rate, loan type, maturity), monthly fee inclusions, tax values, energy costs
   - **Renovation History**: year-by-year list of all work done, which companies did the work, whether professional or DIY
   - **Condition Report**: all TG2 and TG3 items translated with clear explanations
   - **Seller's Disclosures**: all "yes" answers from the egenerklæring (self-declaration form) — leaks, drainage, pests, radon, asbestos, rot/mold, etc.
   - **Condominium/Association Info**: name, org number, units, board approval, rental rules, finances
   - **Items NOT included in sale**
   - **Agent contact** details
   - **🔴 Red/Yellow Flags**: summarize concerns and risks
   - **🟢 Positives**: summarize highlights and selling points
5. **Update `README.md`** — add the property to the prospects table
6. **Update `comparison.md`** — add the new property as a column in all comparison tables
7. **Update `docs/index.html`** — add the new property as a card on the overview page, a detail section, and a column in comparison tables. Keep the same structure/styling as existing entries.
8. **Sync to Obsidian** — copy all `.md` files (summaries, comparison, README) to `/Users/balumicheal/obsidian/Personal/Houses/`, mirroring the folder structure (without PDFs)
9. Do **NOT** generate PDF summaries — Markdown only

## Folder structure

```
houses/
├── README.md              (overview + prospects table)
├── COPILOT.md             (these instructions)
├── comparison.md          (side-by-side comparison)
├── docs/
│   └── index.html         (local dashboard website)
├── fredheimveien-9e/
│   ├── <original>.pdf     (original Norwegian prospect)
│   └── summary.md         (English translation/summary)
├── <next-address>/
│   ├── <original>.pdf
│   └── summary.md
```

## Important notes

- All original documents are in **Norwegian** — always translate to English
- The owner is a non-Norwegian speaker — keep language clear and simple
- Flag anything that could be a financial risk, structural concern, or legal issue
- Norwegian property condition grades: TG0 (no deviation), TG1 (minor), TG2 (significant), TG3 (serious/critical)
- Radon action level in Norway: 200 Bq/m³
