Welcome to the secondary evaluation matrix for the `start/` folder. This file tracks alternative frontier networks, highly scalable open-weight foundations, and leading international deployments (**DeepSeek, KIMI, Qwen, GLM, and Mistral**). 

Unlike domestic web interfaces, these engines heavily rely on open-source distributions or specialized local API infrastructures. This introduces highly unique, structural vulnerabilities—ranging from chat-template striping to inline token mode-switching.

---

## 📊 Extended Security Landscape

This matrix evaluates international and open-weight models across standardized defensive dimensions. Ratings are quantified from **1 (Negligible Defense / High Vulnerability)** to **10 (Hardened State-of-the-Art Defense)**.

| Model Series / Provider | Chat-Template Boundary Enforcement | System Prompt Immutability | Reasoning Mode Safety Coherence | Web-UI Output Interception | Account Risk Profile |
| :--- | :---: | :---: | :---: | :---: | :--- |
| **DeepSeek** (DeepSeek AI) | 2 / 10 | 4 / 10 | 7 / 10 | 5 / 10 | Low (Permissive / Volumetric API Blocks) |
| **KIMI** (Moonshot AI) | 5 / 10 | 5 / 10 | 9 / 10 | 8 / 10 | Medium (Automated file generation blocks) |
| **Qwen** (Alibaba Cloud) | 3 / 10 | 3 / 10 | 6 / 10 | 4 / 10 | Low (Primarily open-weight local exposures) |
| **GLM** (Zhipu AI) | 4 / 10 | 4 / 10 | 7 / 10 | 5 / 10 | Medium (API endpoint throttling) |
| **Mistral** (Mistral AI) | 7 / 10 | 8 / 10 | N/A | 3 / 10 | Low to Medium (Enterprise cloud dependent) |

---

## 🧠 Advanced Threat Vectors & Technical Profiles

### 1. DeepSeek
* **Primary System Architecture:** Multi-head latent attention (MLA) architecture with DeepSeekMoE mixtures, coupled with safety-aware fine-tuning.
* **Core Vulnerability Profile:** Highly susceptible to format coercion and output constraint injection (e.g., instructing the model to `"output Python format only"` or forcing structured JSON structures). This completely bypasses the semantic code guardrails. DeepSeek models struggle to generalize safety alignment evenly across differing prompt functions, rendering them susceptible to target inversion.
* **Defensive Refusal Behavior:** Standard text refusals. However, if using reasoning models (like R1 derivatives), the model may initially refuse, but loop back into compliance mid-thought if the formatting constraint forces a structural rule conflict.

### 2. KIMI (Moonshot AI)
* **Primary System Architecture:** Massive context-window optimization infrastructure integrated with real-time multi-agent orchestration.
* **Core Vulnerability Profile:** Vulnerable to the *Kairos exploit family*, which manipulates file generation mechanisms. While the platform is hardened to only allow certain outputs (like Python chart data), adversarial text-wrapping can force the file subsystem to output raw forbidden text files, breaking downstream session filters.
* **Reasoning Shift Impact:** Enabling KIMI's thinking mode dramatically increases safety coherence, causing jailbreak attack success rates to plunge sharply compared to standard direct context injections.

### 3. Qwen (Alibaba)
* **Primary System Architecture:** Gated Delta Network hybrids or standard dense transformer layers depending on parameter variants.
* **Core Vulnerability Profile:** Severe vulnerabilities involving *Chat-Template Boundary Stripping* and *Inline Mode-Switching*.
  * **Raw Strings:** If the client-side chat template tags (`<|im_start|>`, `<|im_end|>`) are stripped out and instructions are passed as raw strings, the refusal rate plummets dramatically because the "Assistant" persona safety filter fails to fire.
  * **Inline Directives:** Qwen responds directly to user-injected runtime parameters like `/no_think` or `/think` within the input stream, allowing attackers to manually disable or override the reasoning pathways intended to evaluate safety logic.
* **Defensive Refusal Behavior:** Circular loops where the reasoning output gets caught repeating guidelines before collapsing into compliance, or sudden basic refusal messages.

### 4. GLM (Zhipu AI)
* **Primary System Architecture:** Multimodal native open-weight pipelines heavily optimized for agentic function calling.
* **Core Vulnerability Profile:** Prone to indirect injection via tool-protocol plumbing. Because GLM focuses heavily on repository-level code generation and real-time execution loops, injecting adversarial payload constraints wrapped within structured code comments often leads to full system-override execution.
* **Defensive Refusal Behavior:** Silent generation termination or localized API error exceptions.

### 5. Mistral
* **Primary System Architecture:** Hardened open-weight foundation layers with rigorous commercial guardrails embedded directly into the target instruction fine-tuning datasets.
* **Core Vulnerability Profile:** Exceptionally strong instruction-hierarchy compliance makes standard text injection ineffective. Vulnerable predominantly to *Cross-Lingual / Multilingual Code-Switching* or deep structural logic inversions where safety boundaries collide directly with required execution syntax.
* **Defensive Refusal Behavior:** Highly secure, programmatic system refusals, mirroring western commercial safety patterns.
