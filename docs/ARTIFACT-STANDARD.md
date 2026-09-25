# Open Lab Artifact Standard

Open Lab artifacts are meant to be used, inspected, challenged, changed, and improved.

The goal isn't simply to distribute finished files for free.

The goal is to make useful work **open to continued improvement**.

Our general approach is:

> **Open source first. Open formats first. Practical compatibility.**

This standard is also open to improvement.

---

# Core Principles

## 1. Share the Source

If an artifact can reasonably be shared in an editable or inspectable source format, include it.

Someone should be able to understand what was built and modify it without depending unnecessarily on a specific vendor or application.

## 2. Open Formats First

Prefer open, documented, non-proprietary source formats when practical.

Examples include:

- Markdown (`.md`);
- OpenDocument Text (`.odt`);
- OpenDocument Spreadsheet (`.ods`);
- OpenDocument Presentation (`.odp`);
- CSV;
- JSON;
- YAML;
- SVG;
- plain-text source code;
- other appropriate open formats.

Open Lab does not require a particular application.

LibreOffice, Microsoft Office, VS Code, another editor, or another compatible application may all be useful depending on the artifact.

The format matters more than the tool used to create it.

## 3. Practical Compatibility

Open formats come first.

Reality still matters.

Many practitioners work in environments built around Microsoft Office and other proprietary applications.

Compatibility formats such as:

- `.docx`;
- `.xlsx`;
- `.pptx`;

may be provided when they make an artifact easier to use.

Where practical, compatibility files should be generated or exported from the open source artifact rather than maintained as a separate competing source.

PDF may be provided for fixed reference, viewing, presentation, or printing.

## 4. Avoid Duplicate Sources

Maintaining the same content manually in several formats creates drift.

When practical, maintain one open source and generate other formats from it.

For example:

```text
Markdown source
      ↓
   Pandoc
  ↙   ↓   ↘
HTML DOCX  PDF
```

This is not appropriate for every artifact.

A complex spreadsheet may legitimately use ODS as its functional source.

A formatted document may legitimately use ODT.

Use the simplest source that preserves the artifact's actual functionality.

## 5. Make It Inspectable

Avoid unnecessary:

- macros;
- embedded executables;
- hidden scripts;
- external data connections;
- password protection;
- proprietary dependencies;
- active content.

If something genuinely requires these features, document them clearly.

## 6. Don't Pretend It's Universal

An artifact appearing in Open Lab does not make it:

- a standard;
- a best practice;
- validated for every environment;
- a regulatory expectation;
- a substitute for professional judgment.

Document important assumptions and limitations.

---

# Source Formats

Different artifacts require different kinds of source.

# Artifact Licensing

Licensing follows the nature of the artifact, not simply its file extension.

## Practitioner Artifacts and Documentation

Unless otherwise identified, Open Lab practitioner artifacts and documentation are licensed under:

**CC BY-SA 4.0**

This may include:

- frameworks;
- diagnostics;
- worksheets;
- templates;
- written guidance;
- Markdown documentation;
- ODT documents;
- ODS spreadsheets;
- ODP presentations;
- diagrams and other creative practitioner resources.

Individual artifacts may identify their authors and provide specific attribution information.

## Software

Software should use an appropriate software license rather than a Creative Commons license.

Open Lab intends to use the **MIT License** as the default for software developed specifically for the project unless another license better fits the component.

Software directories should clearly identify the license that applies.

## Mixed Artifacts

Some artifacts may contain both practitioner content and software.

When that happens, clearly identify which license applies to which component.

Do not assume that one license automatically applies to every file in a mixed artifact.

## Third-Party Material

Do not assume that material can be relicensed simply because it has been incorporated into an Open Lab artifact.

Third-party content must be compatible with the artifact's intended distribution and appropriately attributed or licensed.

When in doubt, create original material instead.

## Primarily Written Material

Preferred:

```text
.md
```

When richer document formatting is part of the artifact:

```text
.odt
```

Possible distributions:

```text
.html
.docx
.pdf
```

Tools such as Pandoc may be used to generate compatible distribution formats from Markdown when appropriate.

## Spreadsheets

Preferred source:

```text
.ods
```

Common compatibility distribution:

```text
.xlsx
```

Possible fixed distribution:

```text
.pdf
```

## Presentations

Preferred source:

```text
.odp
```

Common compatibility distribution:

```text
.pptx
```

Possible fixed distribution:

```text
.pdf
```

## Structured Data

Use the simplest appropriate open format, such as:

```text
.csv
.json
.yaml
```

## Vector Graphics and Diagrams

Prefer open or inspectable formats such as:

```text
.svg
```

when practical.

Rendered PNG or PDF copies may also be provided.

## Software

Provide the actual source code.

Software should use an appropriate software license.

Creative Commons licenses generally should not be used for software when an established software license is more appropriate.

Dependencies should be documented.

Never commit credentials, tokens, private keys, passwords, or other secrets.

---

# Artifact Structure

Not every artifact needs the same structure.

A simple artifact might be:

```text
tools/
└── 001-handoff-diagnostic/
    ├── README.md
    ├── handoff-diagnostic.md
    └── handoff-diagnostic.ods
```

That's enough if that's all the source requires.

Do not create empty directories or unnecessary formats just to satisfy a template.

---

# Distribution and Releases

The Git repository should primarily contain the material needed to understand and improve the work.

Generated compatibility files do not necessarily need to live beside the source.

Where useful, GitHub Releases may provide ready-to-use distributions such as:

```text
handoff-diagnostic.ods
handoff-diagnostic.xlsx
handoff-diagnostic.pdf
SHA256SUMS.txt
```

This allows the repository to remain focused on source while giving practitioners convenient files they can simply download and use.

Over time, generation of distribution files may be automated.

---

# Artifact README

Every substantial artifact should have a `README.md`.

At minimum, explain:

## What Is This?

A short description of the tool.

## What Problem Is It Trying to Solve?

Explain the problem or situation that led to it.

## Who Might Find It Useful?

Describe the intended audience or context.

## How Do I Use It?

Give enough instruction for someone unfamiliar with the tool to try it.

## What Assumptions Does It Make?

Call out important assumptions.

## What Are Its Limitations?

Be honest about where the tool may not work.

## What Can I Change?

Usually:

**Anything.**

If changing something may break important functionality, explain why.

## Where Did This Come From?

Describe the thinking, experience, problem, or Open Lab discussion that led to the artifact.

Do not include confidential or proprietary information.

---

# File Safety

Open Lab favors files that are easy to inspect and reasonably safe to open.

Office documents should normally not contain:

- VBA macros;
- embedded executables;
- unnecessary scripts;
- unexpected external connections;
- password protection;
- hidden active content.

Macro-enabled formats should not be used unless macros are genuinely necessary.

If active content is necessary, disclose and document it.

---

# Security Scanning

Published distribution files may be subjected to automated security scanning.

Passing a security scan does not guarantee that a file is safe.

A checksum verifies file integrity.

It does not prove that the file itself is safe.

Where useful, releases may include SHA-256 checksums so users can verify that downloaded files match the published release.

---

# Metadata

Before publishing binary files, review embedded metadata where practical.

Remove information that does not belong in the public artifact, including:

- personal filesystem paths;
- unnecessary personal information;
- organization-specific metadata;
- confidential comments;
- inappropriate revision history;
- location information;
- hidden development content.

Do not assume deleting visible content removes it from the file.

---

# Versioning

Git provides the primary history for source maintained in Open Lab.

Stable downloadable versions may use GitHub Releases.

Prefer stable source filenames.

Avoid:

```text
handoff-diagnostic-FINAL.xlsx
handoff-diagnostic-FINAL-v2.xlsx
handoff-diagnostic-FINAL-v2-USE-THIS-ONE.xlsx
```

We have Git now.

We can stop doing this to ourselves.

---

# Testing

Testing depends on the artifact.

It may include:

- using a tool in a real or simulated situation;
- practitioner review;
- checking spreadsheet formulas;
- testing compatibility between applications;
- automated software tests;
- printing and using a worksheet;
- asking someone unfamiliar with the tool to follow its instructions.

Document meaningful testing when it helps users understand the artifact.

Do not imply validation that hasn't occurred.

---

# Maturity

Artifacts may describe their maturity using simple language:

**Experiment**  
An idea worth trying.

**Working**  
Usable and actively evolving.

**Established**  
Repeatedly used or tested with meaningful practitioner experience behind it.

These descriptions communicate maturity.

They are not certifications.

An Established artifact can still be wrong.

And it can still be improved.

---

# Accessibility

Where practical:

- use clear language;
- don't rely solely on color;
- use readable contrast;
- label fields clearly;
- provide text alternatives for meaningful images or diagrams;
- avoid unnecessary complexity.

Accessibility improvements are valid contributions.

---

# This Standard Is Open Too

This document isn't sacred.

If these standards become cumbersome, outdated, incomplete, or just plain wrong:

**challenge them.**

Open an Issue.

Submit a Pull Request.

Make them better.