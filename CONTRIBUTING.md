# Contributing to IBM i Full Stack Explorer

Thanks for taking the time to contribute. This is a community learning resource — every improvement helps someone understand IBM i better.

---

## Ways to contribute

### 1. Fix or improve a layer description

The most valuable contributions. If a beginner or reference description is inaccurate, unclear, or missing important context — open an issue or submit a PR.

Each layer has two descriptions in `index.html`:
- `beginner` — plain English, no assumed knowledge
- `reference` — concise technical details for practitioners

**Good beginner descriptions:**
- Explain the concept from scratch
- Use analogies to familiar technologies (Linux, Windows, cloud)
- Avoid acronyms without defining them first
- 3–5 sentences is the right length

**Good reference descriptions:**
- Lead with the technical name/version
- Include command names, file paths, port numbers, config parameters
- Assume the reader knows IBM i basics
- Use the same key terms IBM documentation uses

---

### 2. Add a toolchain preset

The tool ships with Python/JupyterLab/Django and Node.js/Express/React presets. Other common IBM i integration stacks are welcome:

- Java / Spring Boot / JPA
- .NET / C# / ODBC
- PHP / ODBC
- R / RStudio
- COBOL / traditional green-screen

See [README.md — Customizing the toolchain](README.md#customizing-the-toolchain) for the exact data structure to follow.

---

### 3. Add a new core layer

Layers not yet covered that would be valuable:

- IBM MQ (messaging)
- Db2 Mirror for i (HA/DR)
- IBM i NetServer (SMB/Windows file sharing)
- IBM HTTP Server (Apache on IBM i)
- DDM / DRDA (distributed data)
- Commitment control / journaling (deeper treatment)
- IBM i Services (QSYS2 SQL catalog deep-dive)

Follow the existing layer structure in the `CORE_LAYERS` array.

---

### 4. Add a screenshot or demo GIF

The README has a placeholder for `screenshots/preview.png`. A clean screenshot of the tool with a layer expanded — in both beginner and reference mode — would help new visitors understand what they're looking at.

---

### 5. Translate descriptions

IBM i is global. If you can write accurate beginner/reference descriptions in another language, open an issue to discuss the approach (separate file vs. runtime language toggle).

---

## Submitting a pull request

1. Fork the repo
2. Create a branch: `git checkout -b fix/layer-db2-reference` or `feat/add-java-toolchain`
3. Make your changes to `index.html` (and `README.md` / `CONTRIBUTING.md` if relevant)
4. Open a PR with a clear description of what changed and why

**PR checklist:**
- [ ] Descriptions are factually accurate for IBM i 7.3–7.5
- [ ] Beginner mode uses plain English and no undefined acronyms
- [ ] Reference mode includes specific command/path/parameter names where relevant
- [ ] Tags are concise and genuinely useful (not just keywords)
- [ ] IBM Docs link points to a real, relevant page
- [ ] The Claude prompt is specific enough to get a useful answer
- [ ] The HTML file still opens correctly in a browser with no console errors

---

## Reporting issues

Use GitHub Issues for:
- Incorrect technical information
- Broken links (IBM Docs URLs change)
- Suggestions for new layers or toolchain presets
- UI bugs

Please include:
- Which layer and which mode (beginner/reference)
- What is currently wrong or missing
- What the correct information should be (with a source if possible)

---

## Code style

This is a single HTML file — no build tools, no linters, no framework. Keep it that way. Contributions should:

- Not introduce external dependencies (CDN links, npm packages)
- Keep the file openable offline in any modern browser
- Follow the existing naming conventions in the `CORE_LAYERS` and `STACKS` objects
- Not break the Beginner/Reference toggle or toolchain switcher

---

## Questions?

Open an issue tagged `question`. There are no gatekeepers here — if you're unsure whether something is a good contribution, just ask.
