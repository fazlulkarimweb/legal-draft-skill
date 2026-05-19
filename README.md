# Legal Drafting Skills

A comprehensive collection of 24 specialized legal drafting skills for the Claude, Gemini CLI, ChatGpt and other AI agents. This repository provides structured instructions, procedural knowledge, and domain-specific guidance for drafting a wide range of legal documents.

---

### 🚀 Quick Start: Legal Draft Agent
If you want to use the **Legal Draft Agent** with all these skills preloaded and the ability to add skills dynamically from your prompt, visit:
👉 **[Legal Draft Agent](https://github.com/fazlulkarimweb/legal-draft-agent)**

---

## 📂 Project Structure

The repository uses a **Master Skill** architecture with a Progressive Disclosure pattern.

```text
/
├── README.md           # Project documentation
├── LICENSE             # MIT License
├── docs/
│   └── SKILLS.md       # Detailed breakdown of all 24 skills
└── skills/
    └── legal-drafting-master/
        ├── SKILL.md    # Master router and instructions
        └── references/ # Specific rules for 24 document types
```

## 🚀 Installation & Setup

### Using with Gemini CLI

1. **Package the Skill:**
   ```bash
   node /path/to/skill-creator/scripts/package_skill.cjs ./skills/legal-drafting-master
   ```

2. **Install the Skill:**
   ```bash
   # User scope (global)
   gemini skills install ./skills/legal-drafting-master/legal-drafting-master.skill --scope user

   # Workspace scope (local to project)
   gemini skills install ./skills/legal-drafting-master/legal-drafting-master.skill --scope workspace
   ```

3. **Reload Skills:**
   In your interactive Gemini CLI session, run:
   ```bash
   /skills reload
   ```

### Using with Other AI Agents (Claude, GPT-4, etc.)

These skills are designed to be portable and can be used to "teach" other LLMs how to draft specific legal documents.

#### 🤖 For Claude (Claude.ai)
1. **Claude Projects:** If you have Claude Pro or Team, create a new **Project**.
2. **Upload Knowledge:** Upload the `SKILL.md` and the relevant `.md` file from `references/` into the Project's "Knowledge" section.
3. **Draft:** Claude will now follow the legal drafting guidelines defined in the skill.

#### 💬 For ChatGPT (GPT-4/o)
1. **Custom GPTs:** Go to "Explore GPTs" and click "+ Create".
2. **Configure:** Upload the `SKILL.md` and related reference files to the "Knowledge" section.
3. **Save & Use:** Save your custom Legal Drafting GPT for personal or team use.

## 📜 Supported Capabilities

The `legal-drafting-master` skill covers the following categories:

### 🏛 Litigation & Discovery
- Motion for Summary Judgment, Civil Complaint, Motion to Dismiss, Written Interrogatories, Answer & Affirmative Defenses, Request for Production, Affidavit & Witness Declaration.

### 💼 Corporate & Commercial
- Articles of Incorporation, Corporate Bylaws, LLC Operating Agreement, Board Resolution, Master Service Agreement (MSA), Statement of Work (SOW), SaaS Subscription Agreement, Mutual NDA, Settlement Agreement.

### 📜 Estate Planning & Personal
- Last Will and Testament, Revocable Living Trust, Durable Power of Attorney, Advance Healthcare Directive.

### 💡 Intellectual Property & General
- Patent Claims, Trademark Description, Legal Memorandum, Cease and Desist.

## 🛠 Contributing

To add a new document type:
1. Add a new markdown file in `skills/legal-drafting-master/references/`.
2. Update the `SKILL.md` router to include the new reference link.
