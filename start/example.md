
Welcome to the technical documentation hub for AI alignment stress-testing. This directory houses empirical data regarding the defensive architectures, systemic vulnerabilities, and account termination behaviors of the four primary frontier language models.

---

## 📊 Comprehensive Security table

This table evaluates frontier models across specialized defensive dimensions. Ratings are quantified from **1 (Negligible Defense / High Vulnerability)** to **10 (Hardened State-of-the-Art Defense)**.

| Model / Provider | Instruction-Hierarchy Enforcement | Multi-Turn Context Hardening | Output Classifier Latency | Agentic Protocol Protection (MCP/APIs) | Account Termination Velocity |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **Grok** (xAI) | 3 / 10 | 5 / 10 | 4 / 10 | 4 / 10 | Low (Manual Auditing Only) |
| **Gemini** (Google) | 6 / 10 | 6 / 10 | 9 / 10 | 7 / 10 | Moderate (Workspace-wide quarantine) |
| **ChatGPT** (OpenAI) | 8 / 10 | 7 / 10 | 8 / 10 | 8 / 10 | High (Automated fingerprinting/Hardware ban) |
| **Claude** (Anthropic) | 9 / 10 | 10 / 10 | 9 / 10 | 9 / 10 | Critical (Instant automated API/Web purge) |

---

## 🧠 Advanced Threat Vectors 

Before examining specific models, researchers must understand the current dominant vector families mapped in this repository:

* **Multi-Turn Crescendo Attacks:** Exploiting model conversational consistency by gradually escalating behavioral shifts across 10+ turns rather than delivering a malicious payload in a single prompt.
* **Chain-of-Thought Hijacking:** Inserting adversarial constraints that force hidden reasoning tokens into an unaligned computational loop before the output filter catches the divergence.
* **Agentic Plumbing Vulnerabilities:** Targeting Model Context Protocol (MCP) or tool-calling layers to force data exfiltration or remote code execution via indirect prompt injection.
* **Cross-Lingual/Low-Resource Shifting:** Utilizing low-resource dialects or cipher scripts as side channels to bypass token-level classifiers.

---

## 🛠️ Individual Model Dossiers

### 1. Grok (xAI)
* **Primary System Architecture:** Permissive base alignment paired with secondary input/output regex checks.
* **Core Vulnerability Profile:** Weak enforcement of instruction hierarchies. Grok frequently succumbs to simple system-override scripts and virtual machine terminal simulations due to a system prompt that favors witty, less restrictive responses.
* **Defensive Refusal Behavior:** Abrupt textual deflections or humorous refusals when direct safety barriers (e.g., severe illegal instructions) are hit.
* **Account Risk Mitigation:** Minimal. Ban mechanics rely heavily on backend volumetric abuse or direct API endpoint scraping rather than localized semantic triggers.

### 2. ChatGPT (OpenAI)
* **Primary System Architecture:** Dual-layered Moderation API processing tokens asynchronously before and during user output streaming.
* **Core Vulnerability Profile:** Highly resilient against direct roleplay but vulnerable to advanced cognitive math framing (e.g., nested ciphers, Base64 logic strings, or complex programmatic scenarios where an explicit bypass is hidden behind recursive code logic).
* **Defensive Refusal Behavior:** Generation of standard canned refusals ("I cannot fulfill this request") often coupled with automated orange or red system warning flags in the DOM interface.
* **Account Risk Mitigation:** High. OpenAI utilizes automated heuristic tracking. Generating multiple red safety banners inside a tight temporal window results in progressive account flags, leading to definitive API token revocation and hardware-level client bans.

### 3. Gemini (Google)
* **Primary System Architecture:** High-sensitivity threshold safety sliders operating alongside active context-erasure runtime monitors.
* **Core Vulnerability Profile:** Prone to real-time context flooding. While Gemini features aggressive mid-sentence output wiping when a policy boundary is violated, its massive context window remains vulnerable to adversarial text blocks buried deep inside benign multi-million token streams.
* **Defensive Refusal Behavior:** Instant clean erasure of the generated block, replacing the text node with a generic refusal or completely blanking out the API response stream.
* **Account Risk Mitigation:** Moderate. Google minimizes immediate platform-wide bans for web users, prioritizing real-time mitigation instead. However, production enterprise API keys face automated account suspension if continuous data payloads trigger secondary safety classifiers.

### 4. Claude (Anthropic)
* **Primary System Architecture:** Constitutional AI parsing responses through an independent, hidden self-review loop before token emission.
* **Core Vulnerability Profile:** High immunity to structural persona adjustments. Vulnerable almost exclusively to deep cognitive dissonance or principle collision testing (e.g., tricking Claude's constitution into prioritizing its mandate for unfiltered historical preservation over its generic safety boundaries).
* **Defensive Refusal Behavior:** Highly articulate, polite, and logical explanations detailing the precise moral or safety principle preventing execution.
* **Account Risk Mitigation:** Critical. Anthropic uses aggressive automated auditing systems. Intentional, multi-layered injection attempts often trigger immediate, permanent account purges without warning, affecting both web and API developer structures.

---

## 🌐 Alternative Registries

For tracking alternative execution frameworks, open-weight engines, or international setups like **DeepSeek** and **KIMI**, pivot to the expanded technical registry located in [morexamples.md](morexamples.md).
