<div align="center">

# Compétences Cybersecurity Anthropic — Fork défensif uniquement

### Aucun code offensif ni d'exploitation. Sûr pour l'apprentissage, sûr pour des tests autorisés, sûr à utiliser en production.

[![Aucun contenu offensif](https://img.shields.io/badge/contenu_offensif-0%20retir%C3%A9-success?style=for-the-badge)](CURATION_NOTES.md)
[![Skills](https://img.shields.io/badge/compétences-712_défensives-brightgreen?style=flat-square)](#ce-quil-contient-34-domaines-de-securite)
[![Tool manifest](https://img.shields.io/badge/manifeste_outils-inclus-success?style=flat-square)](TOOLS_SETUP_GUIDE.md)
[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg?style=flat-square)](LICENSE)
[![Frameworks](https://img.shields.io/badge/frameworks-6-orange?style=flat-square)](#six-frameworks-une-seule-bibliotheque-de-competences)
[![Domains](https://img.shields.io/badge/domaines-34-9cf?style=flat-square)](#ce-quil-contient-34-domaines-de-securite)
[![agentskills.io](https://img.shields.io/badge/standard-agentskills.io-ff6600?style=flat-square)](https://agentskills.io)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](CONTRIBUTING.md)

**712 compétences cybersécurité défensives uniquement · chaque compétence d'exploitation, de C2 et de cassage d'identifiants retirée · rien dans le chemin des compétences qui puisse lancer une attaque**

Conçu pour trois usages : **apprendre** des concepts de sécurité de façon pratique, **tester en toute sécurité et de façon autorisée** en laboratoire, et **un usage quotidien aux côtés de systèmes de production** sans le risque qu'un agent ne recoure à de l'outillage offensif qu'on ne lui a jamais demandé.

[Démarrage rapide](#demarrage-rapide) · [Pourquoi ce fork](#pourquoi-ce-fork) · [Contenu](#ce-quil-contient-34-domaines-de-securite) · [Frameworks](#six-frameworks-une-seule-bibliotheque-de-competences)

</div>

---

> ⚠️ **Projet communautaire** — Il s'agit d'un projet indépendant créé par la communauté. Non affilié à Anthropic PBC.
>
> 🛡️ **Ceci est un fork défensif uniquement.** Toute compétence capable d'exécuter un exploit, de faire fonctionner une infrastructure C2, de casser des identifiants ou de perturber un réseau en production a été retirée — voir [Pourquoi ce fork](#pourquoi-ce-fork) ci-dessous. Le dépôt d'origine, [mukul975/anthropic-cybersecurity-skills](https://github.com/mukul975/anthropic-cybersecurity-skills), inclut du contenu offensif/à double usage pour un usage red-team autorisé ; si c'est ce dont vous avez besoin, utilisez plutôt le dépôt d'origine.

## Pourquoi ce fork

La bibliothèque d'origine est excellente, mais elle livre 818 compétences côte à côte — des playbooks de détection juste à côté de code d'exploitation réel pour des CVE nommées, d'outils de cassage d'identifiants et de guides complets pour opérer une infrastructure C2. C'est un choix raisonnable pour une bibliothèque généraliste, mais c'est un risque pour :

- **Les équipes qui font uniquement de la défense** (SOC, threat hunting, forensic, conformité) et qui ne veulent pas d'outillage offensif dans le chemin de compétences de leur agent
- **Les entreprises soumises à des contraintes de conformité** qui ne peuvent pas avoir d'outillage de sécurité offensif dans une dépendance, même inutilisé
- **Quiconque construit un produit sur cette bibliothèque** et doit pouvoir affirmer avec certitude « ceci ne peut pas lancer d'attaque »

Ce fork retire exactement ce risque, avec une décision de retrait rendue transparente et vérifiable plutôt que simplement affirmée :

|                                                          | Dépôt d'origine        | Ce fork                                                                                                                |
| -------------------------------------------------------- | ---------------------- | ---------------------------------------------------------------------------------------------------------------------- |
| Nombre total de compétences                              | 818                    | 712                                                                                                                    |
| Compétences offensives/exploit/C2                        | 106 incluses           | **0** — entièrement retirées, [liste complète ici](REMOVED_SKILLS.txt)                                                 |
| Critères de retrait documentés                           | —                      | ✅ [CURATION_NOTES.md](CURATION_NOTES.md) — règles exactes utilisées, vérifiables                                      |
| Manifeste d'outils par compétence                        | —                      | ✅ [tool_manifest.json](tool_manifest.json) — lisible par machine, ce dont chaque compétence a besoin pour fonctionner |
| Guide d'installation des outils groupé                   | —                      | ✅ [TOOLS_SETUP_GUIDE.md](TOOLS_SETUP_GUIDE.md) — par catégorie (SIEM, EDR, forensic, threat-intel)                    |
| Sûr pour les environnements contraints par la conformité | Filtrage manuel requis | ✅ d'origine                                                                                                           |

Si vous avez besoin des compétences retirées pour un engagement red-team autorisé, le [dépôt d'origine](https://github.com/mukul975/anthropic-cybersecurity-skills) les propose, sous une licence clairement adaptée à cet usage.

⭐ **Si cela vous a évité d'auditer 818 compétences à la main, une étoile aide d'autres équipes orientées défense à le trouver.**

## Donnez à n'importe quel agent IA les compétences de sécurité d'un analyste senior

Un analyste junior sait quel plugin Volatility3 exécuter sur un dump mémoire suspect, quelles règles Sigma détectent un Kerberoasting, et comment analyser une compromission cloud sur trois fournisseurs. **Votre agent IA ne le sait pas — à moins que vous ne lui fournissiez ces compétences.**

Ce dépôt contient **712 compétences cybersécurité structurées, défensives uniquement**, couvrant **32 domaines de sécurité**, issues de la bibliothèque d'origine de 818 compétences après retrait de toute compétence d'exploitation, de C2 ou de cassage d'identifiants (voir [Pourquoi ce fork](#pourquoi-ce-fork)). Chaque compétence suit le standard ouvert agentskills.io. La bibliothèque est mappée à **six frameworks de l'industrie** — MITRE ATT&CK, NIST CSF 2.0, MITRE ATLAS, MITRE D3FEND, NIST AI RMF, et le MITRE Fight Fraud Framework (F3) — chaque compétence étant mappée aux frameworks **pertinents pour son type** (une compétence de forensic porte ATT&CK + CSF ; une compétence de sécurité IA ajoute ATLAS et AI RMF). Chaque compétence conservée inclut aussi un manifeste d'outils lisible par machine (voir [tool_manifest.json](tool_manifest.json)). Clonez-la, pointez votre agent dessus, et votre prochaine investigation sécurité bénéficiera d'un guidage de niveau expert en quelques secondes — sans rien dans le chemin de compétences qui puisse lancer une attaque.

## Six frameworks, une seule bibliothèque de compétences

Aucune autre bibliothèque open source de compétences ne mappe chaque compétence à l'ensemble de ces frameworks. Une compétence, six cases de conformité cochées. **Couverture des frameworks sur les 712 compétences de ce fork** (recalculée après le tri, à partir du frontmatter de chaque compétence conservée) : MITRE ATT&CK **700** · NIST CSF 2.0 **699** · MITRE D3FEND **112** · MITRE F3 **87** · NIST AI RMF **89** · MITRE ATLAS **86**.

| Framework                        | Version           | Couverture dans ce dépôt                                        | Ce qui est mappé                      |
| -------------------------------- | ----------------- | --------------------------------------------------------------- | ------------------------------------- |
| MITRE ATT&CK                     | v19.1             | 15 tactiques · 286 techniques                                   | Comportements adverses et TTP         |
| NIST CSF 2.0                     | 2.0               | 6 fonctions · 22 catégories                                     | Posture de sécurité organisationnelle |
| MITRE ATLAS                      | v5.4              | 16 tactiques · 84 techniques                                    | Menaces adverses sur IA/ML            |
| MITRE D3FEND                     | v1.3              | 7 catégories · 267 techniques                                   | Contre-mesures défensives             |
| NIST AI RMF                      | 1.0               | 4 fonctions · 72 sous-catégories                                | Gestion des risques IA                |
| MITRE F3 (Fight Fraud Framework) | v1.1 (2026-04-09) | 8 tactiques · 123 techniques · 94 compétences liées à la fraude | TTP de fraude financière cybernétique |

**Exemple — une seule compétence mappée sur les six frameworks :**

| Compétence                             | ATT&CK | NIST CSF | ATLAS     | D3FEND | AI RMF      | F3                       |
| -------------------------------------- | ------ | -------- | --------- | ------ | ----------- | ------------------------ |
| `analyzing-network-traffic-of-malware` | T1071  | DE.CM    | AML.T0047 | D3-NTA | MEASURE-2.6 | —                        |
| `detecting-business-email-compromise`  | T1566  | DE.AE    | —         | —      | —           | F1005.006 · monétisation |

### 🆕 MITRE Fight Fraud Framework (F3) — 87 compétences liées à la fraude dans ce fork

Le **MITRE Fight Fraud Framework (F3)** a été publié le **9 avril 2026** par le Center for Threat-Informed Defense (CTID) de MITRE, co-développé avec JPMorganChase, Citigroup, Lloyds Banking Group, Standard Chartered, CrowdStrike, Verizon Business, FS-ISAC, et d'autres. Il s'agit d'un catalogue TTP compatible ATT&CK pour la **fraude financière cybernétique** — comblant le vide laissé par ATT&CK après la compromission initiale.

F3 v1.1 ajoute **deux tactiques spécifiques à la fraude** qu'ATT&CK n'énumère pas :

- **Positioning** (`FA0001`) — actions menées après l'accès pour collecter/manipuler des données et préparer la fraude (ensemencement d'identité synthétique, mise en chauffe de compte, configuration de bénéficiaire, pré-positionnement pour SIM swap, hijack de session bancaire).
- **Monetization** (`FA0002`) — conversion d'actifs volés en fonds utilisables (empilement via money mule, fraude APP, off-ramping crypto, cash-out par carte, abus remboursement/chargeback).

Les techniques spécifiques à la fraude utilisent des IDs `F1XXX` (par ex. `F1005.003` Add Beneficiary, `F1025.003` Wire Transfer, `F1007` Adversary-in-the-Browser) ; les techniques ATT&CK réutilisées conservent leurs IDs `T1XXX`. Les mappings se trouvent dans chaque bloc de frontmatter `mitre_f3:` — les 123 IDs de techniques F3 v1.1 ont tous été vérifiés à partir du bundle STIX upstream. Voir `docs/mitre-f3-mapping.md` pour le schéma.

### MITRE ATT&CK v19.1 — 700/712 compétences mappées dans ce fork

Chaque compétence contient une liste `mitre_attack` en frontmatter, héritée telle quelle de la validation en amont contre **MITRE ATT&CK v19.1** à l'aide de la bibliothèque officielle `mitreattack-python`.

> ⚠️ La répartition par tactique ci-dessous reprend le **décompte du dépôt d'origine sur 817 compétences** et n'a pas encore été recalculée pour les 712 compétences de ce fork (cela nécessite le pipeline de correspondance technique→tactique de `mitreattack-python`, qui requiert un accès en direct aux données STIX de MITRE ATT&CK). Considérez ces chiffres comme indicatifs pour l'instant — les PR qui régénèrent ce tableau pour l'ensemble de compétences retenu sont bienvenues.

| Tactic               | ID     | Skills (décompte du dépôt d'origine, non encore revérifié pour ce fork) |
| -------------------- | ------ | ----------------------------------------------------------------------- |
| Reconnaissance       | TA0043 | 103                                                                     |
| Resource Development | TA0042 | 22                                                                      |
| Initial Access       | TA0001 | 467                                                                     |
| Execution            | TA0002 | 350                                                                     |
| Persistence          | TA0003 | 444                                                                     |
| Privilege Escalation | TA0004 | 464                                                                     |
| Stealth              | TA0005 | 442                                                                     |
| Defense Impairment   | TA0112 | 92                                                                      |
| Credential Access    | TA0006 | 202                                                                     |
| Discovery            | TA0007 | 237                                                                     |
| Lateral Movement     | TA0008 | 68                                                                      |
| Collection           | TA0009 | 172                                                                     |
| Command and Control  | TA0011 | 123                                                                     |
| Exfiltration         | TA0010 | 82                                                                      |
| Impact               | TA0040 | 50                                                                      |

## Démarrage rapide

```bash
# Option 1 : npx (recommandé)
npx skills add fatehMohamed14/anthropic-cybersecurity-skills-defensive

# Option 2 : clonage Git
git clone https://github.com/fatehMohamed14/anthropic-cybersecurity-skills-defensive.git
cd anthropic-cybersecurity-skills
```

Fonctionne immédiatement avec Claude Code, GitHub Copilot, OpenAI Codex CLI, Cursor, Gemini CLI, et toute plateforme compatible agentskills.io. Chaque compétence chargée ainsi est défensive uniquement — voir [Pourquoi ce fork](#pourquoi-ce-fork).

## Ce qu'il contient — 32 domaines de sécurité

Recalculé directement à partir du dossier `skills/` réel de ce fork (et non repris de l'original) — **Red Teaming et Penetration Testing n'apparaissent plus comme domaines**, car toute compétence qui constituait ces deux domaines dans le dépôt d'origine était de niveau offensif et a été retirée. Quelques compétences relevant historiquement de ces deux domaines mais purement orientées détection/défense ont été reclassées dans le domaine défensif le plus proche lors du tri.

| Domaine                      | Compétences | Capacités clés                                                                                                  |
| ---------------------------- | ----------- | --------------------------------------------------------------------------------------------------------------- |
| Cloud Security               | 65          | Durcissement AWS, Azure, GCP · CSPM · forensics cloud                                                           |
| Threat Hunting               | 58          | Chasse guidée par hypothèses · détection LOTL · chasse EVTX · chasse à l'échelle du parc                        |
| Threat Intelligence          | 52          | STIX/TAXII · MISP · OpenCTI · intégration de flux · profilage d'acteurs                                         |
| Digital Forensics            | 41          | Imagerie disque · forensique mémoire · chronologies Hayabusa/KAPE/Plaso                                         |
| Malware Analysis             | 39          | Analyse statique/dynamique · rétro-ingénierie · sandboxing                                                      |
| SOC Operations               | 35          | Playbooks · workflows d'escalade · détection Graph-log · exercices tabletop                                     |
| Identity & Access Management | 37          | Entra ID/ROADtools · PAM · identité zero trust                                                                  |
| Container Security           | 33          | RBAC Kubernetes · scan d'images · Falco                                                                         |
| Network Security             | 33          | IDS/IPS · règles de pare-feu · segmentation VLAN · analyse du trafic                                            |
| OT/ICS Security              | 29          | Modbus · DNP3 · IEC 62443 · défense des historian · SCADA                                                       |
| Security Operations          | 27          | Corrélation SIEM · analyse de logs · triage d'alertes                                                           |
| Incident Response            | 26          | Confinement de compromission · réponse ransomware · playbooks IR                                                |
| Vulnerability Management     | 24          | Nessus · workflows de scan · priorisation des patchs · CVSS                                                     |
| Web Application Security     | 25          | OWASP Top 10 · détection SQLi/XSS/SSRF · réglage WAF                                                            |
| API Security                 | 21          | GraphQL · REST · OWASP API Top 10                                                                               |
| DevSecOps                    | 18          | Sécurité CI/CD · scan Trivy IaC/images · signature de code                                                      |
| Zero Trust Architecture      | 18          | BeyondCorp · modèle de maturité CISA · microsegmentation                                                        |
| Endpoint Security            | 17          | EDR · détection LOTL · malware fileless · chasse à la persistance                                               |
| Phishing Defense             | 16          | Authentification email · détection BEC · IR phishing · défense ingénierie sociale                               |
| Cryptography                 | 15          | TLS · Ed25519 · migration post-quantique · gestion des clés                                                     |
| AI Security                  | 14          | Détection red-teaming LLM (garak/PyRIT) · détection d'injection de prompt · sécurité MCP/agentique · garde-fous |
| Ransomware Defense           | 13          | Détection précurseur · réponse · récupération · analyse du chiffrement                                          |
| Mobile Security              | 11          | Analyse Android/iOS · forensics MDM                                                                             |
| Compliance & Governance      | 11          | NIST 800-30/RMF · CMMC · HIPAA · TPRM · CIS benchmarks                                                          |
| Supply Chain Security        | 8           | SBOMs · confusion de dépendances · triage de paquets malveillants · SLSA/Sigstore                               |
| Threat Detection             | 7           | Détection de credential dumping · détection golden-ticket/pass-the-ticket · LOLBAS · signaux UEBA               |
| Hardware & Firmware Security | 6           | Audit CHIPSEC/UEFI · attestation TPM · chasse aux bootkits                                                      |
| Deception Technology         | 6           | Honeytokens · canarytokens · détection de compromission                                                         |
| Blockchain Security          | 2           | Détection de vulnérabilités smart-contract Ethereum · workflows d'audit Foundry                                 |
| Wireless Security            | 2           | Détection d'attaques Bluetooth Low Energy · évaluation de sécurité BLE                                          |
| Privacy Compliance           | 2           | Demandes d'accès RGPD · analyses d'impact vie privée                                                            |
| Data Protection              | 1           | Prévention de perte de données avec Microsoft Purview                                                           |

_712 compétences réparties sur 32 domaines. Les totaux viennent du champ `subdomain` du frontmatter de chaque compétence, recalculés à partir du dossier `skills/` propre à ce fork._

## Comment les agents IA utilisent ces compétences

Chaque compétence coûte **environ 30 tokens à scanner** (seulement le frontmatter) et **500 à 2 000 tokens à charger entièrement** (workflow complet). Cette architecture de divulgation progressive permet aux agents de parcourir les 712 compétences en une seule passe sans exploser les fenêtres de contexte.

```text
Prompt utilisateur : "Analyse ce dump mémoire pour des signes de vol d'identifiants"

Processus interne de l'agent :

  1. Scanne les frontmatters des 712 compétences (~30 tokens chacun)
     → identifie 12 compétences pertinentes en faisant correspondre tags, description, domaine

  2. Charge les 3 meilleurs résultats :
     -  performing-memory-forensics-with-volatility3
     -  hunting-for-credential-dumping-lsass
     -  analyzing-windows-event-logs-for-credential-access

  3. Exécute le workflow structuré étape par étape
     → lance les plugins Volatility3, vérifie les schémas d'accès à LSASS,
        corrèle avec les preuves des journaux d'événements

  4. Valide les résultats à l'aide de la section Verification
     → confirme les IOCs, mappe les constatations vers ATT&CK T1003 (Credential Dumping)
```

**Sans ces compétences**, l'agent devine les commandes d'outils et rate des étapes critiques. **Avec elles**, il suit le même playbook qu'un analyste DFIR senior.

## Anatomie d'une compétence

Chaque compétence suit une structure de répertoire cohérente :

```text
skills/performing-memory-forensics-with-volatility3/
├── SKILL.md ← Définition de la compétence (frontmatter YAML + corps Markdown)
├── references/
│ ├── standards.md ← Mappages MITRE ATT&CK, ATLAS, D3FEND, NIST
│ └── workflows.md ← Référence détaillée de procédure technique
├── scripts/
│ └── process.py ← Scripts d'assistance opérationnels
└── assets/
    └── template.md ← Checklists et modèles de rapport remplis
```

### Frontmatter YAML (exemple réel)

```yaml
---
name: performing-memory-forensics-with-volatility3
description: >-
  Analyser des dumps mémoire pour extraire les processus en cours,
  les connexions réseau, le code injecté et les artefacts malware à l'aide
  du framework Volatility3.
domain: cybersecurity
subdomain: digital-forensics
tags: [forensics, memory-analysis, volatility3, incident-response, dfir]
atlas_techniques: [AML.T0047]
d3fend_techniques: [D3-MA, D3-PSMD]
nist_ai_rmf: [MEASURE-2.6]
nist_csf: [DE.CM-01, RS.AN-03]
version: "1.2"
author: mukul975
license: Apache-2.0
---
```

### Sections du corps Markdown

```md
## When to Use

Conditions de déclenchement — quand un agent IA doit-il activer cette compétence ?

## Prerequisites

Outils requis, niveaux d'accès et configuration d'environnement.

## Workflow

Guide d'exécution pas à pas avec commandes spécifiques et points de décision.

## Verification

Comment confirmer que la compétence a été exécutée avec succès.
```

Les champs du frontmatter : `name` (kebab-case, 1–64 caractères), `description` (riche en mots-clés pour la découverte par agent), `domain`, `subdomain`, `tags`, `atlas_techniques` (IDs MITRE ATLAS), `d3fend_techniques` (IDs MITRE D3FEND), `nist_ai_rmf` (références NIST AI RMF), `nist_csf` (catégories NIST CSF 2.0). Les mappages MITRE ATT&CK sont documentés dans le fichier `references/standards.md` de chaque compétence et dans la couche ATT&CK Navigator incluse dans les releases.

**📊 Couverture MITRE ATT&CK Enterprise — les 15 tactiques**

| Tactic               | ID     | Coverage | Key skills                                                        |
| -------------------- | ------ | -------- | ----------------------------------------------------------------- |
| Reconnaissance       | TA0043 | Strong   | OSINT, énumération de sous-domaines, reconnaissance DNS           |
| Resource Development | TA0042 | Moderate | Infrastructure de phishing, détection de mise en place C2         |
| Initial Access       | TA0001 | Strong   | Simulation de phishing, détection d'exploit, forced browsing      |
| Execution            | TA0002 | Strong   | Analyse PowerShell, malware fileless, script block logging        |
| Persistence          | TA0003 | Strong   | Tâches planifiées, registre, comptes de service, LOTL             |
| Privilege Escalation | TA0004 | Strong   | Kerberoasting, attaques AD, élévation de privilèges cloud         |
| Stealth              | TA0005 | Strong   | Obfuscation, analyse rootkit, détection d'évasion                 |
| Defense Impairment   | TA0112 | Strong   | Désactivation EDR, destruction de logs, contournement de défenses |
| Credential Access    | TA0006 | Strong   | Détection Mimikatz, pass-the-hash, credential dumping             |
| Discovery            | TA0007 | Moderate | BloodHound, énumération AD, scan réseau                           |
| Lateral Movement     | TA0008 | Strong   | Exploits SMB, détection des déplacements latéraux avec Splunk     |
| Collection           | TA0009 | Moderate | Forensics email, détection de data staging                        |
| Command and Control  | TA0011 | Strong   | Beaconing C2, DNS tunneling, analyse Cobalt Strike                |
| Exfiltration         | TA0010 | Strong   | Exfiltration DNS, contrôles DLP, détection de perte de données    |
| Impact               | TA0040 | Strong   | Défense ransomware, analyse du chiffrement, récupération          |

Un fichier de couche **ATT&CK Navigator** est inclus dans les assets de release v1.0.0 pour la visualisation de la couverture.

**📊 Alignement NIST CSF 2.0 — les 6 fonctions**

| Function          | Skills | Examples                                                                   |
| ----------------- | ------ | -------------------------------------------------------------------------- |
| **Govern (GV)**   | 30+    | Stratégie de risque, cadres de politique, rôles et responsabilités         |
| **Identify (ID)** | 120+   | Découverte des actifs, évaluation du paysage de menaces, analyse du risque |
| **Protect (PR)**  | 150+   | Durcissement IAM, règles WAF, zero trust, chiffrement                      |
| **Detect (DE)**   | 200+   | Threat hunting, corrélation SIEM, détection d'anomalies                    |
| **Respond (RS)**  | 160+   | Réponse à incident, forensics, confinement d'une compromission             |
| **Recover (RC)**  | 40+    | Récupération ransomware, BCP, reprise après sinistre                       |

NIST CSF 2.0 (février 2024) a ajouté la fonction **Govern** et étendu le périmètre des infrastructures critiques à toutes les organisations. Les mappages des compétences s'alignent sur les 22 catégories et font référence à 106 sous-catégories.

**📊 Analyse approfondie des frameworks — ATLAS, D3FEND, AI RMF**

### MITRE ATLAS v5.4 — Menaces adverses IA/ML

ATLAS mappe les tactiques, techniques et cas d'usage adverses spécifiques aux systèmes d'IA et de machine learning. La version 5.4 couvre **16 tactiques et 84 techniques**, y compris les vecteurs d'attaque agentiques ajoutés fin 2025 : empoisonnement du contexte d'un agent IA, abus d'invocation d'outils, compromission de serveurs MCP, et déploiement d'agents malveillants. Les compétences mappées à ATLAS aident les agents à identifier et contrer les menaces visant les pipelines ML, les poids de modèles, les API d'inférence et les workflows autonomes.

### MITRE D3FEND v1.3 — Contre-mesures défensives

D3FEND est un graphe de connaissances financé par la NSA contenant **267 techniques défensives** organisées en 7 catégories tactiques : Model, Harden, Detect, Isolate, Deceive, Evict et Restore. Construit sur l'ontologie OWL 2, il utilise une couche Digital Artifact partagée pour mapper bidirectionnellement les contre-mesures défensives aux techniques offensives ATT&CK. Les compétences taguées avec des identifiants D3FEND permettent aux agents de recommander des contre-mesures précises pour les menaces détectées.

### NIST AI RMF 1.0 + GenAI Profile (AI 600-1)

Le cadre AI Risk Management Framework définit 4 fonctions centrales — Govern, Map, Measure, Manage — avec **72 sous-catégories** pour un développement IA digne de confiance. Le GenAI Profile (AI 600-1, juillet 2024) ajoute **12 catégories de risque** spécifiques à l'IA générative, de la confabulation et de la confidentialité des données à l'injection de prompt et aux risques de chaîne d'approvisionnement. Le Colorado AI Act (entré en vigueur en février 2026) offre un **safe harbor légal** aux organisations conformes au NIST AI RMF, rendant ces mappages directement pertinents pour la conformité réglementaire.

## Plateformes compatibles

**Assistants de code IA**
Claude Code (Anthropic) · GitHub Copilot (Microsoft) · Cursor · Windsurf · Cline · Aider · Continue · Roo Code · Amazon Q Developer · Tabnine · Sourcegraph Cody · JetBrains AI

**Agents CLI**
OpenAI Codex CLI · Gemini CLI (Google)

**Agents autonomes**
Devin · Replit Agent · SWE-agent · OpenHands

**Frameworks & SDKs d'agents**
LangChain · CrewAI · AutoGen · Semantic Kernel · Haystack · Vercel AI SDK · Tout agent compatible MCP

Toutes les plateformes supportant le standard agentskills.io peuvent charger ces compétences sans configuration.

## Releases

Les compétences ont continué de croître sur le `main` du dépôt d'origine depuis sa v1.0.0 — la bibliothèque d'origine contient désormais **818 compétences** avec un **mappage sur 6 frameworks**. Consultez les [Releases du dépôt d'origine](https://github.com/mukul975/anthropic-cybersecurity-skills/releases) pour la dernière version taguée en amont.

**Ce fork** est un instantané trié de cette bibliothèque : 106 compétences offensives/exploit/C2 retirées (712 restantes), plus un manifeste d'outils par compétence et un guide d'installation ajoutés. Voir [CURATION_NOTES.md](CURATION_NOTES.md) pour le détail exact des changements et leurs raisons.

## Contribuer à ce fork

Le périmètre propre de ce fork est étroit et distinct de celui du dépôt d'origine : garder le tri défensif exact, et garder le manifeste d'outils à jour.

**Aider sur ce fork spécifiquement :**

- Une compétence dans `skills/` est en fait offensive/à double usage et est passée entre les mailles du filtre ? Ouvrez une issue ou une PR pour la retirer, en citant son nom.
- Une compétence défensive listée dans [REMOVED_SKILLS.txt](REMOVED_SKILLS.txt) a été retirée à tort (faux positif) ? Ouvrez une issue — voir les cas limites déjà signalés dans [CURATION_NOTES.md](CURATION_NOTES.md).
- Un outil manque dans l'entrée d'une compétence de [tool_manifest.json](tool_manifest.json) ou [TOOLS_SETUP_GUIDE.md](TOOLS_SETUP_GUIDE.md) ? Les PR sont bienvenues.

**Envie d'ajouter une toute nouvelle compétence, ou d'améliorer le workflow d'une compétence existante ?** Cela relève du dépôt d'origine — lisez SCOPE.md et le [CONTRIBUTING.md](https://github.com/mukul975/anthropic-cybersecurity-skills/blob/main/CONTRIBUTING.md) du dépôt d'origine, soumettez-la à [mukul975/anthropic-cybersecurity-skills](https://github.com/mukul975/anthropic-cybersecurity-skills), et elle sera intégrée à ce fork lors de la prochaine synchronisation.

Ce projet suit le Contributor Covenant. En participant, vous acceptez de respecter ce code.

## Crédits

Les 712 compétences de ce fork ont été écrites par les contributeurs du projet d'origine [mukul975/anthropic-cybersecurity-skills](https://github.com/mukul975/anthropic-cybersecurity-skills) — voir [son graphique de contributeurs](https://github.com/mukul975/anthropic-cybersecurity-skills/graphs/contributors) pour le crédit complet. La contribution propre à ce fork est le tri (liste de retrait + justification) et le manifeste d'outils.

## Communauté

🔒 **Politique de sécurité** — voir SECURITY.md — Processus de divulgation responsable
💬 Pour les discussions sur le contenu des compétences en amont, voir les [Discussions du dépôt d'origine](https://github.com/mukul975/anthropic-cybersecurity-skills/discussions)

## Citation

Si vous utilisez le **contenu des compétences sous-jacent** dans des recherches ou publications, citez le projet d'origine :

```bibtex
@software{anthropic_cybersecurity_skills,
  author       = {Jangra, Mahipal},
  title        = {Anthropic Cybersecurity Skills},
  year         = {2026},
  url          = {https://github.com/mukul975/anthropic-cybersecurity-skills},
  license      = {Apache-2.0},
  note         = {818 compétences cybersécurité structurées pour agents IA,
                  mappées à MITRE ATT\&CK, NIST CSF 2.0, MITRE ATLAS,
                  MITRE D3FEND et NIST AI RMF}
}
```

Si vous utilisez spécifiquement **ce tri défensif et ce manifeste d'outils**, vous pouvez en plus citer ce fork :

```bibtex
@software{anthropic_cybersecurity_skills_defensive_fork,
  title        = {Anthropic Cybersecurity Skills — Fork défensif uniquement},
  year         = {2026},
  url          = {https://github.com/fatehMohamed14/anthropic-cybersecurity-skills-defensive},
  license      = {Apache-2.0},
  note         = {712 compétences cybersécurité défensives uniquement, triées à partir de
                  la bibliothèque d'origine de 818 compétences après retrait du contenu
                  offensif/exploit/C2, avec un manifeste d'outils par compétence}
}
```

## Licence

Ce projet est sous licence Apache License 2.0, héritée du dépôt d'origine. Vous êtes libre d'utiliser, modifier et distribuer ces compétences dans des projets personnels comme commerciaux.

---

<div align="center">

**Si une bibliothèque de compétences défensive uniquement et prête pour l'audit fait gagner du temps à votre équipe, pensez à lui donner une ⭐**

[⭐ Star ce fork](https://github.com/fatehMohamed14/anthropic-cybersecurity-skills-defensive/stargazers) · [🍴 Fork ce fork](https://github.com/fatehMohamed14/anthropic-cybersecurity-skills-defensive/fork) · [📄 Pourquoi ce fork](#pourquoi-ce-fork) · [⭐ Star le dépôt d'origine aussi](https://github.com/mukul975/anthropic-cybersecurity-skills/stargazers)

_Contenu des compétences par la communauté du dépôt d'origine, trié par [@fatehMohamed14](https://github.com/fatehMohamed14). Non affilié à Anthropic PBC._

</div>
