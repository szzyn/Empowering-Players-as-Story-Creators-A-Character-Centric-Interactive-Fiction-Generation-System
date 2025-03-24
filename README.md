# 📘 CMN'25 — *Empowering Players as Story Creators: A Character-Centric Interactive Fiction Generation System*

This repository contains the full set of prompt templates and evaluation materials used in our CMN'25 paper:  
**"Empowering Players as Story Creators: A Character-Centric Interactive Fiction Generation System" (.pdf)**

The study introduces a character-centric interactive storytelling system that integrates **VIA (Values in Action)** and the **Big Five personality traits** to improve coherence, creativity, and emotional engagement in story generation.  
We present a working prototype and pilot study that demonstrate the effectiveness of using character personality traits in generating dynamic, branching narratives with large language models.

---

## 🧩 Abstract (from CMN'25 paper)

> Interactive storytelling empowers users to shape narratives dynamically through active co-creation. This study introduces a character-centric story generation framework that incorporates VIA (Values in Action) and the Big Five personality traits model to improve narrative coherence, immersion, and creativity. The system generates branching stories within an interactive fiction framework, utilizing language models to tailor story progression based on user choices. We implement a prototype and conduct a pilot study, demonstrating that character-centric branching significantly enhances narrative depth and engagement. Future work will focus on parameter optimization and the refinement of prompt engineering techniques, with the goal of enhancing interactive novel generation.

---

## 🧾 Prompt Templates

This section includes the exact prompts used for each experimental condition.

### 🔹 Entry 1 – **Logline-Based Branching (No Personality Traits)**
- **Description**: Branches are generated using only the logline, without integrating any character personality traits.
- **Files**:
  - `entry1_branch_prompt.txt` – Prompt used for generating next-branch options at each turn.

---

### 🔹 Entry 2 – **Character Personality-Based Branching (VIA + Big Five)**
- **Description**: Branches are generated using both the logline and selected character personality traits (3 VIA + Big Five scores).
- **Files**:
  - `entry2_branch_prompt.txt` – Prompt template including VIA + Big Five inputs and previous story context.

---
 🔹 `entry12_story_generatino_prompt.txt` – Prompt used to generate a story based on selected branch at Entry 1 and 2.



### 🔹 Entry 3 – **Logline-Based Linear Story**
- **Description**: A fully linear (non-branching) story generated based only on the logline.
- **Files**:
  - `entry3_story_generation_prompt.txt` – Prompt used to produce a complete narrative in a single pass.

---

## 🧪 Evaluation Prompts

We evaluated all generated narratives using both **human evaluators** and **LLMs (GPT-4o, Claude 3.5 Sonnet, LLaMA 3 8B)**.

for branch evaluation
- `evaluation_prompt_gpt.txt`  
- `evaluation_prompt_llama.txt`  
- `evaluation_prompt_claude.txt`  

Each prompt asks the LLM to evaluate two dimensions on a 5-point Likert scale:  
**Consistency** and **Appropriateness**

for story evaluation
- `story_evaluation_prompt_gpt.txt`  
- `story_evaluation_prompt_llama.txt`  
- `story_evaluation_prompt_claude.txt`  

Each prompt asks the LLM to evaluate five narrative dimensions on a 5-point Likert scale:  
**Coherence**, **Creativity**, **Engagement**, **Trait Alignment**, and **Logline Appropriateness**.



