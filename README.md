# SPMS Claim Packer

A website for SPMS committee claims: https://ghostofsouls.github.io/spms-claims-maker/

- **Pack a claim:** drop in receipts, payment screenshots and the event budget sheet. AI reads each one, converts everything to PDFs named `Vendor (Item) Receipt - $Amount.pdf`, sorts them into `SAO/` and `SPMS Office/`, and downloads the claim zip.
- **FinCon: read a claim zip:** pulls the amount, receipt number, date and invoice number from every receipt in a zip, ready to copy into ICS.

Everything runs in the browser. Files only go to the AI the user picks: free keys from Google Gemini, OpenRouter or Groq, or paid Claude API / OpenAI keys. Busy models are retried, then the page switches to another model. Keys are stored only in that browser, and only if the user ticks "Remember".

AI is optional: every field can be typed by hand.

For AI agents and screen readers, every control has an accessible name and the page carries a hidden step-by-step guide. [llms.txt](llms.txt) has the same steps as plain text.
