# Cx Credits Calculator: versions

The calculator is released with CxMissionZero and carries its version (MZ-xx.xx.xx). Newest first.

## MZ-01.01.08 — 2026-11-09

- **Three Fusion tabs, one estimate in the credits.** Fusion · Checkmarx One, Fusion · from Git and Fusion · cloc-fusion each open with what they found and their credits. **Use this instead** picks the one in the credits, so the same code is never counted twice. **Leave Fusion out** takes Fusion out of the credits.
- **Fusion pricing explains a zero.** It marks the model the projects use and says when that model has no price, which is why Fusion credits stayed 0.
- **Several Git tokens.** Fusion · from Git takes one token after another. It recognises GitHub, GitLab and Bitbucket from the token, finds each token's organisations and repositories, counts a repository that two tokens can see once, and counts them all in one go. The tokens are never saved or printed.
- **Customer ▾.** One menu lists the customers, with New, Rename and Delete. When there is no customer, one is made straight away and named after Your organisation. **Apply** is always in the settings block.
- **The report compares, and lists by project.** **Fusion estimates side by side** shows each estimate worked out, with the one in the credits marked (in the PDF too). **Open vulnerabilities by project** adds each project's open findings by severity to the appendix.
- **Your customers come back.** The calculator opens at the same address every run (127.0.0.1:47317), so the customers saved in the browser come back. A read from Checkmarx One says how far it is and how long is left.
- **Watch the read, and work while it runs.** A panel on the right names each project as Checkmarx One is read, with the totals climbing. Triage & remediation and Fusion · Checkmarx One fill in from the first projects in, so the severities, the period and the prices can be tried before the read ends.
- **Git tokens beside the API key.** Paste git tokens next to the Checkmarx One key, ready for Fusion · from Git.
- **Status.** All 1,033 tests pass, and `npm audit --omit=dev` finds nothing.
