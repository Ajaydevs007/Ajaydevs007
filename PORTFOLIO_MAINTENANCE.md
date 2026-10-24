# Cybersecurity Portfolio Maintenance Workflow

Use this checklist whenever adding a new lab or learning note. The goal is to keep the portfolio accurate, evidence-backed, safe to publish, and easy to navigate.

## 1. Choose the right repository

| Work item | Repository |
|---|---|
| Hack The Box machines, authorized penetration tests, VAPT methodology | [VAPT](https://github.com/Ajaydevs007/VAPT) |
| SOC labs, alert investigations, SIEM work, detections, reports, and playbooks | [SOC Analyst Journey](https://github.com/Ajaydevs007/soc-analyst-journey) |
| Protocols, ports, packet analysis, network fundamentals | [Networking Notes](https://github.com/Ajaydevs007/networking-notes) |
| Linux filesystem, commands, permissions, and foundational Linux topics | [Linux File System Guide](https://github.com/Ajaydevs007/linux-file-system-guide) |
| Portfolio landing page and cross-repository navigation | [GitHub profile repository](https://github.com/Ajaydevs007/Ajaydevs007) |

Do not create a new repository or an empty Cloud Security folder just to reserve a name. Add Cloud Security material when a practical lab has been performed and can be documented with evidence.

## 2. Use the relevant documentation checklist

### HTB / VAPT walkthrough

- Record the platform, machine name, operating system, difficulty, and completion status accurately.
- Document scope and the initial enumeration before describing an attack path.
- Separate commands, observations, interpretations, findings, and remediation.
- Link to detailed enumeration, exploitation, privilege-escalation, and command notes where needed.
- Use only evidence actually captured. Add a brief caption explaining what each screenshot demonstrates.
- Do not publish flags, passwords, tokens, cookies, private keys, or raw sensitive captures.

### SOC investigation

- State the alert or investigation question, data source, time range, and relevant telemetry.
- Include the query, explain each important filter and aggregation, and record the observed result.
- Document triage reasoning, a timeline where useful, relevant ATT&CK mapping, impact, and next actions.
- Distinguish lab-generated activity from real incidents, and distinguish validated results from hypotheses.
- Link related detections, incident reports, playbooks, evidence, and the parent project README.

### Detection rule

- Document the behavior to detect, required logs/fields, query, thresholds, grouping, and time window.
- Explain why the logic is useful and identify likely false positives and tuning considerations.
- Record how it was tested and whether an alert/incident was actually generated.
- Include a representative sanitized result or screenshot when available.
- Do not label a rule “validated” or “production-ready” solely because the query was saved.

### Networking note

- Define the concept and identify relevant protocols, ports, packet fields, or command examples.
- State the security or SOC relevance and include a small, safe example where helpful.
- Link topic files from the Networking Notes README only after those files exist.

### Linux topic

- Explain the path, command, permission, or concept and show safe example usage.
- Identify distribution/version assumptions when behavior can vary.
- Include security implications, especially for logs, system configuration, permissions, and privilege boundaries.
- Link new topic files from the Linux guide when they exist; avoid duplicating a complete explanation already maintained elsewhere.

### Cloud Security lab — only after hands-on work

- Identify the cloud provider, services, lab objective, architecture, and permissions actually configured.
- Document the test, logs or controls observed, detection or hardening steps, and evidence.
- Record cost and cleanup steps, including how to remove lab resources.
- Never commit cloud credentials, access keys, client secrets, state files containing secrets, or private configuration.
- Add the result to the profile only after the lab is complete enough to describe honestly.

## 3. Screenshot and evidence standard

- Use descriptive, stable names, such as `01-nmap-services.png` or `03-sentinel-incident.png`, when naming new screenshots.
- Preserve existing filenames unless renaming is needed and every reference is updated.
- Before committing, inspect each image for passwords, flags, tokens, cookies, email addresses, account IDs, connection strings, or other private data.
- Redact sensitive values without removing the context needed to interpret the evidence.
- Do not commit raw PCAPs, exported credential lists, flag files, or private configuration.
- Keep a short evidence index in the project's README. Link to real files rather than suggested filenames that are not present.

## 4. Documentation and link checks before publishing

1. Read the existing README and relevant files before changing anything.
2. Update the most local index first, then the parent repository README, then the profile README if the work is a meaningful featured project.
3. Verify every new relative link against the current repository tree and open important external links.
4. Preview Markdown tables, code fences, image paths, and long filenames.
5. Review the diff for unrelated changes and accidental duplicate content.
6. Search staged content for likely secrets, including `password`, `token`, `secret`, `api_key`, `.env`, private keys, and flag patterns. Inspect context manually; a keyword scan is not a substitute for reviewing the actual content and images.
7. Check that the README status reflects what the evidence proves. Use “planned” for unstarted work, “in progress” for ongoing work, and “completed” only when the stated scope is done.
8. Commit with a concise message that describes the documentation or lab change.

For substantial changes, prefer a dedicated branch and pull request so the diff can be reviewed before merging. For small, clearly scoped corrections, keep the change limited and verify it immediately afterward.

## 5. Keep repository roles distinct

- **Profile README:** short landing page, selected projects, current learning, certifications, and contact links.
- **SOC Analyst Journey:** defensive labs, alert investigations, detection logic, incident reports, and playbooks.
- **VAPT:** offensive-security practice and HTB walkthroughs.
- **Networking Notes:** networking concepts and packet-analysis foundations.
- **Linux File System Guide:** Linux filesystem and command-line foundations.

Link related work across repositories; do not copy the same full write-up into multiple places. Update cross-links when a project is renamed or moved.

## 6. Final pre-publish checklist

- [ ] Claims match completed work and available evidence.
- [ ] No credentials, tokens, flags, private configuration, or sensitive screenshots are included.
- [ ] Query results and screenshots are sanitized.
- [ ] Relative links and image paths resolve.
- [ ] The relevant index and profile cross-links are updated.
- [ ] No accidental empty files, duplicate write-ups, or unrelated changes were introduced.
