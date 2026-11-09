# Cx Credits Calculator

The credits a Checkmarx One customer needs for **Triage & remediation** of their backlog and for **Checkmarx Fusion** scans, worked out from their own data, with a report and a PDF summary to send them.

This repository holds the calculator **as people download and run it**. It is built from [CxMissionZero](https://github.com/cxsmtp/CxDetectionDateBaseReminder), where the same calculator runs inside the app (Plan → Cx Credits Calculator) from the same code; changes are made there and each release is published here.

| File | What it is |
| --- | --- |
| [`cx-credits-calculator.mjs`](cx-credits-calculator.mjs) | The calculator with a small launcher: reads Checkmarx One with an API key and counts code from git, on your computer. Needs Node.js 20 or later. |
| [`cx-credits-calculator.html`](cx-credits-calculator.html) | The calculator as one HTML file, for a computer without Node.js: works from the two Checkmarx One exports, makes the same reports. |

## Run it

```
node cx-credits-calculator.mjs
```

It opens the calculator in your browser at `http://127.0.0.1:47317/`, the same address every run, so the customers you saved come back next time. Ctrl+C stops it. Stop the one running before starting it again (a second copy starts on another port and does not show the customers saved before). `--port 8080` picks another port, `--no-open` only prints the address.

Behind TLS inspection, set `NODE_EXTRA_CA_CERTS` to your company's root certificate first. Counting code from git uses git 2.31 or later when it is installed, or the platforms' APIs.

## What it does

- **Customer ▾**: your customers, each saved as you go in the browser, with New, Rename and Delete. **Back up** saves them all as one file; **Restore** brings them back, in that browser or another.
- **Checkmarx One API key**: paste it and **Connect**; **Read from Checkmarx One** reads every project with its lines of code, criticality, scans and backlog (it shows how far it is, and how long is left).
- **Projection settings**: every branch or the primary one, projects to read, scan origins, projects and applications, the projection period, extra credits and bundles. **Apply** works every figure out again.
- **Triage & remediation**: the backlog by severity, its trend, the findings still to come, and the credits to triage and remediate them, with the false positives assumed.
- **Three Fusion tabs, one estimate in the credits**:
  - **Fusion · Checkmarx One**: the projects already in Checkmarx One, their Fusion scans from how often each was scanned in the last 12 months;
  - **Fusion · from Git**: the customer's repositories counted from git with one or more read-only tokens (GitHub, GitLab, Azure DevOps, Bitbucket), their Fusion scans from how often each changes;
  - **Fusion · cloc-fusion**: a report the customer makes with cloc-fusion where their code is, or cloc results.
  
  **Use this instead** picks the estimate counted, so the same code is never counted twice. **Fusion pricing** holds each model's credits per 10K lines of code: each project's lines are rounded up to whole 10K blocks, and a Fusion scan costs its model's credits per block.
- **Credits required**: Triage & remediation and Fusion together, the extra credits on top, and the bundles.
- **The report**: one HTML file with the answer first, how it was worked out, the assumptions and every figure; the customer can try other numbers in it. Options: **Include project names and details**, **Fusion estimates side by side**, **Open vulnerabilities by project**. **Download PDF summary** gives the pages to present.

## Where your data goes

- The page is served on 127.0.0.1 only and answers only itself.
- The Checkmarx One key and the git tokens are held in the launcher's memory for that run only: never saved, logged or put in a report.
- Customers and reports are kept in your browser (IndexedDB), nowhere else.
- The calculator talks to Checkmarx One, and to the git hosts you give tokens for; nothing else.

## Licence period

The calculator works until 31 December 2026 (UTC), as CxMissionZero does, unless the product activation code is entered.

## Version

See [CHANGELOG.md](CHANGELOG.md).
