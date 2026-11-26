# Luxembourg Form 100 – an agent skill for your income tax return

Give this skill to your AI agent and it can help you with the Luxembourg personal income tax return (Form 100) for **tax year 2025**. It explains the rules in plain words, walks you through the return box by box, estimates your tax, fills in the official PDF, builds the file MyGuichet imports, and goes through a checklist with you before you sign.

Made by [BravoLisa](https://bravolisa.lu). Free to use, change and share, also commercially – see [Licence](#licence).

## What it covers

- **Who:** employees, pensioners, cross-border workers (France, Belgium, Germany) and self-employed people – residents and non-residents.
- **What:** tax class and joint taxation, the tax scale, tax credits, salary certificates, special expenses (insurance, pension plans, home savings, donations), childcare and other abatements, your own home and mortgage interest, single parents, marriage, separation, divorce or death during the year.
- **Every rule has a label and a source:** confirmed by an official text, our interpretation, practice, or still open – with links to the law, the forms and the tax office's pages.
- **Tools** (Python): tax estimate, Form 100 PDF filler, MyGuichet import file (checked against the tax office's schema), and a reader for the PDF MyGuichet gives back.

**Not included:** computing a business profit (Forms 152 and 110), VAT, social-security contributions and company taxes. A self-employed person brings their profit from their own forms or accountant – or uses BravoLisa's larger skill, [luxembourg-self-employed-accounting](https://github.com/bravolisa/luxembourg-self-employed-accounting-skill), which holds all of that and everything in this one.

## Status

**An experiment.** BravoLisa built this skill with the help of AI agents. This is version 0.50.1 of its knowledge base, built on 2026-11-26. Forms and tools are for tax year 2025, with 2026 figures where known. It is general information that an AI applies, not tax advice, and it can be wrong or out of date. You check, sign and file your own return. By installing or using the skill you accept the [licence](LICENSE.md) and the [terms of use](TERMS.md).

## Install

**Claude Code**

```
/plugin marketplace add bravolisa/luxembourg-form-100-skill
/plugin install luxembourg-form-100@bravolisa
```

Or copy the folder `skills/luxembourg-form-100` into `~/.claude/skills/`.

**Claude apps (claude.ai, desktop)**: zip the folder `skills/luxembourg-form-100` and upload the zip under Settings → Capabilities → Skills. Code execution must be on for the tools.

**Other agents**: give the agent the folder `skills/luxembourg-form-100` and tell it to start with `SKILL.md`.

**Tools**: Python 3.9 or later. From the skill folder: `python3 -m venv .venv` and `.venv/bin/pip install -r lu-annual-return/scripts/requirements.txt`.

## Try it

- "Help me prepare our 2025 Luxembourg tax return. We are married, both employed, with one child born in 2025."
- "Which Form 100 box does my private pension plan go in, and how much can I deduct for 2025?"
- "I'm a French resident working in Luxembourg. Do I have to file Form 100?"
- "Here is my tax bulletin. Does it match my return?"

## Rather not do it yourself?

| | Price (VAT included) | How |
|---|---|---|
| **Do it in BravoLisa's app** – upload your documents, Lisa fills in Form 100 | Free to prepare, €34 to download the PDF and the MyGuichet file | https://bravolisa.lu/form-100 |
| **A person checks your finished return** against your documents, and later your tax bulletin | €99 per tax year | alex@bravolisa.lu |
| **An accountant prepares, signs and files it** for you | Price on request | alex@bravolisa.lu |

Details and limits: [BRAVOLISA.md](skills/luxembourg-form-100/BRAVOLISA.md).

## Licence

Free to use for any purpose, also a commercial one: for yourself, in your business, for your clients, in your own product or service. You may copy it, change it and share it. The summary is in [LICENSE.md](LICENSE.md).

- **The texts** (rules, figures, guides): [CC BY 4.0](LICENSE-CC-BY-4.0.txt). When you share them, or texts made from them, credit BravoLisa with a link and say if you changed them.
- **The tools** (the Python code): [Apache 2.0](LICENSE-APACHE-2.0.txt). Keep [NOTICE.txt](NOTICE.txt) and the copyright lines in the files.

If you build on this, please say "Tax and accounting knowledge: BravoLisa" with a link to https://bravolisa.lu.

The name and logo "BravoLisa" are not licensed. The ACD's blank form and schema in `official-forms/` belong to the ACD.

## Errors and updates

Found an error or an outdated rule? Open an issue here or write to alex@bravolisa.lu.

This repository is generated from BravoLisa's internal knowledge base. Pull requests are read but cannot be merged directly – the fix goes in through the knowledge base and appears here with the next update.
