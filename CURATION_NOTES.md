# Curation Notes — Defensive-Only Fork

This fork of `mukul975/anthropic-cybersecurity-skills` has had **106 offensive/dual-use skills removed**, leaving **712 defensive, detection, forensics, and compliance skills**.

## How removal was decided

A skill was removed if either was true:

1. Its `subdomain` frontmatter tag was `red-teaming`, `penetration-testing`, `purple-team`, `offensive-security`, or `red-team`.
2. Its folder name matched an action-verb pattern associated with live exploitation, credential theft, C2 infrastructure, or network disruption (`exploiting-`, `attacking-`, `bypassing-`, `coercing-`, `abusing-`, `operating-*-c2`, `performing-*-attack`, `conducting-*-simulation`, etc).

See `/home/claude/removal_list.txt`-equivalent — the full removed list is in `REMOVED_SKILLS.txt` in this folder, for your review.

## ⚠️ Review these before trusting the cut

A handful of removed skills are lower-risk than most of this list (mostly passive recon or standard vulnerability scanning) and you may want to restore them from the original repo if you have a legitimate, authorized use case:

- `conducting-external-reconnaissance-with-osint`, `performing-open-source-intelligence-gathering` — passive OSINT, no system contact
- `performing-vulnerability-scanning-with-nessus`, `conducting-api-security-testing` — standard scanning, authorized-use-only but industry-standard
- `performing-purple-team-atomic-testing` — collaborative detection validation (Atomic Red Team), commonly run safely in enterprise environments
- `performing-iot-security-assessment`, `performing-physical-intrusion-assessment` — assessment-framework skills, not raw exploits

Everything else on the removed list (exploit code for named CVEs, C2 frameworks, credential cracking, network-disruptive attacks, live phishing-send campaigns) should stay out unless you have a dedicated, isolated lab and a clear authorized-testing reason to restore it.

## What's left

712 skills across: cloud security, threat hunting, threat intelligence, network security, web app security (detection/testing-for-* variants, not exploiting-* variants), digital forensics, malware analysis, IAM, SOC operations, incident response, vulnerability management, DevSecOps, zero-trust, endpoint security, cryptography, phishing defense, AI security, mobile security, ransomware defense, compliance/governance, and supply-chain security.

## Tooling

See `TOOLS_SETUP_GUIDE.md` for a grouped list of every tool/platform referenced across the kept skills, and `tool_manifest.json` for the exact tool list per individual skill (machine-readable, keyed by skill folder name).
