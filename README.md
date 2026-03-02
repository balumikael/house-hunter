# 🏠 House/Apartment Prospects

This folder contains prospects (prospekter) for potential houses and apartments we are considering buying in Norway.

## Instructions for Copilot

When a new Norwegian property prospect PDF is added to this folder:

1. **Create a subfolder** named after the address in kebab-case (e.g., `fredheimveien-9e/`)
2. **Move the PDF** into that subfolder
3. **Extract text** from the PDF using PyPDF2 (install if needed: `pip install PyPDF2`)
4. **Create a Markdown summary** (`summary.md`) in the subfolder, translated to English, containing:
   - At-a-glance table (price, fees, total cost, size, rooms, year, energy rating)
   - Property description & layout
   - Key features
   - Location & transport info
   - Financial details (cost breakdown, shared debt, monthly fees, tax values, energy costs)
   - Renovation history
   - Condition report highlights (TG2/TG3 issues)
   - Seller's disclosures (leaks, drainage, pests, radon, asbestos, etc.)
   - Condominium/housing association info & finances
   - Items not included in sale
   - Agent contact details
   - **🔴 Red/Yellow flags** — things to watch out for
   - **🟢 Positives** — highlights and selling points
5. **Update this README** — add the property to the prospects table below
6. Do **NOT** generate a PDF summary — Markdown only

## Folder Structure

```
houses/
├── README.md
├── fredheimveien-9e/
│   ├── prospekt fredheimveien 9 e.pdf   (original Norwegian)
│   └── summary.md                        (English translation)
├── <next-property>/
│   ├── <original>.pdf
│   └── summary.md
```

## Prospects

| # | Property | Asking Price | Size | Folder |
|---|----------|-------------|------|--------|
| 1 | Fredheimveien 9E, Oslo (Høybråten) | 7,550,000 NOK | 146 m² | [fredheimveien-9e](fredheimveien-9e/) |
| 2 | Løkendalen 72, Skedsmokorset (Lillestrøm) | 6,990,000 NOK | 147 m² | [lokendalen-72](lokendalen-72/) |
| 3 | Konvallveien 7, Lørenskog (Finstadjordet) | 7,390,000 NOK | 142 m² | [konvallveien-7](konvallveien-7/) |
| 4 | Lillehauger 5, Bærum (Kolsås) | 7,990,000 NOK | 128 m² | [lillehauger-5](lillehauger-5/) |
