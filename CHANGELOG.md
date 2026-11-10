# Cx Credits Calculator: versions

The calculator is released with CxMissionZero and carries its version (MZ-xx.xx.xx). Newest first.

## MZ-01.01.08 — 2026-11-09

- **Three Fusion tabs, one estimate in the credits.** Fusion · Checkmarx One, Fusion · from Git and Fusion · cloc-fusion each open with what they found and their credits. **Use this instead** picks the one in the credits, so the same code is never counted twice. **Leave Fusion out** takes Fusion out of the credits.
- **Fusion pricing explains a zero.** It marks the model the projects use and says when that model has no price, which is why Fusion credits stayed 0.
- **Several Git tokens.** Fusion · from Git takes one token after another. It recognises GitHub, GitLab and Bitbucket from the token, finds each token's organisations and repositories, counts a repository that two tokens can see once, and counts them all in one go. The tokens are never saved or printed.
- **Customer ▾.** One menu lists the customers, with New, Rename and Delete. When there is no customer, one is made straight away and named after Your organisation. **Apply** is always in the settings block.
- **The report lists by project.** Only the Fusion estimate in the credits is in the report and the PDF. **Open vulnerabilities by project** adds each project's open findings by severity to the appendix.
- **Your customers come back.** The calculator opens at the same address every run (127.0.0.1:47317), so the customers saved in the browser come back. A read from Checkmarx One says how far it is and how long is left.
- **Watch the read, and work while it runs.** A panel on the right names each project as Checkmarx One is read, with the totals climbing. Triage & remediation and Fusion · Checkmarx One fill in from the first projects in, so the severities, the period and the prices can be tried before the read ends.
- **Git tokens beside the API key.** Paste git tokens next to the Checkmarx One key, ready for Fusion · from Git.
- **A % for what is still to come.** **New findings counted (%)** sets how many new findings to count: 100% keeps the last months' pace, 50% half, 0% none. Still to come shows the sum, for example 525 a month × 11.9 months × 50%.
- **No clicks after the keys.** Connect reads Checkmarx One. A git token given beside the key counts everything it can see on Fusion · from Git by itself. Once the read starts, the keys and settings fold into one line with the read's bar, so the credits come first.
- **The highest Fusion estimate by itself.** The estimate predicting the most credits is in them until you pick another with Use this instead. The three Fusion tabs look alike.
- **The gap to close, in the report.** The debt rate shows in dark red and the fixing rate in dark green. Gap to close, the points between them, is highlighted in dark red.
- **Your data stays with you.** Customers, reports and the names on the reports are saved to `cx-credits-calculator-data.json` in the folder you start the calculator from, made the first time and loaded the next; a small line under the head says where and when it last saved.
- **A next-gen look.** The calculator and its report open in a futuristic dark, cyan and violet on deep space, with a light version on the theme button; the PDF summary has white pages under a deep-space band, its key figures in cyan to violet and a coloured chart. **Try other numbers** in the report is one line under the total until opened, and Generate projection report and Download PDF summary stay on the line of the report options.
- **Status.** All 1,037 tests pass, and `npm audit --omit=dev` finds nothing.
