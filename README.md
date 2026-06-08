Progressive Project Scoping Funnel

A lightweight discovery skill for scoping software, product, and technical projects through three focused questions.

The goal is to surface just enough signal to create a useful project baseline without making the human feel like they are filling out a heavy requirements form.

This skill helps identify:

* The core pain the project should remove
* The main delivery tradeoff
* The hidden risk most likely to derail the work
* Any contradictions between ambition, constraints, and risk
* The most useful immediate next technical step

⸻

What This Is

The Progressive Project Scoping Funnel is a low-friction project discovery workflow.

It guides a user through three short questions:

1. Pain — What frustrating, slow, expensive, or error-prone thing should disappear?
2. Tradeoff — If things get harder than expected, what can flex: scope, budget, or timeline?
3. Risk — What hidden issue could quietly derail the project?

After those questions, the assistant generates a concise Project Baseline Document.

⸻

Why Use It

Most project scoping processes either ask too many questions too early or jump straight into solutions before the real constraints are clear.

This skill is designed to strike a better balance.

It keeps the surface experience simple while still extracting useful architectural and planning signals.

Use it when you want to:

* Scope a new software or product project
* Clarify an idea before implementation
* Prepare for technical architecture planning
* Identify hidden delivery risks
* Create a lightweight project baseline
* Avoid premature technology decisions
* Align stakeholders around the real problem

⸻

Expected Output

The final synthesis produces a short project baseline with:

* Core Pain to Remove
* Likely Shape of the Project
* Flex Point
* Main Risk to Design Around
* Tension Check
* Open Assumptions
* Recommended Next Step

The output is intentionally concise. It is meant to guide the next technical decision, not replace a full project plan.

⸻

Files

Recommended package structure:

three-questions/
├── SKILL.md
└── README.md

For ChatGPT Skill uploads, the package may also include platform metadata depending on the final packaging workflow.

⸻

Installation for ChatGPT

Option 1: Use as a ChatGPT Skill

1. Create a folder named:

three-questions

2. Add the following files to the folder:

SKILL.md
README.md

3. Zip the folder.
    The zip should preserve the folder structure:

three-questions.zip
└── three-questions/
    ├── SKILL.md
    └── README.md

4. Upload the zip through ChatGPT’s Skills interface.
5. Once installed, start a conversation with a prompt such as:

Help me scope a new software project.

    or:

Use the progressive project scoping funnel for this idea.

Option 2: Use as a Plain Prompt

If you are not using ChatGPT Skills, copy the contents of SKILL.md into a conversation and then say:

Run this project scoping funnel with me.

This works well for one-off use, though it will not be reusable across conversations unless saved elsewhere.

⸻

Installation for Claude

Claude does not use ChatGPT Skill packages directly, but the same workflow can be used as a Claude Project instruction or as a reusable prompt.

Option 1: Add to a Claude Project

1. Create a new Claude Project.
2. Open the Project instructions.
3. Paste the contents of SKILL.md into the instructions.
4. Optionally upload or paste this README.md as supporting documentation.
5. Start a new chat inside the Project and say:

Help me scope a new software project.

Claude should then follow the three-question funnel as part of the Project behavior.

Option 2: Use as a Claude Prompt

1. Open a new Claude chat.
2. Paste the contents of SKILL.md.
3. Add:

Please follow this workflow and start the scoping session.

This is best for occasional use.

Option 3: Use as a Claude Project Knowledge File

If you prefer keeping the main Project instructions shorter:

1. Add a short Project instruction such as:

When the user asks to scope, plan, or de-risk a software/product project, follow the Progressive Project Scoping Funnel from the attached knowledge file.

2. Upload SKILL.md as a Project knowledge file.
3. Upload this README.md as optional supporting context.

This keeps the Project instructions lightweight while preserving the full workflow.

⸻

Suggested Invocation Prompts

Use any of the following prompts to start the workflow:

Help me scope a new project.
Run the project scoping funnel for this idea.
I have a product idea and want to turn it into a technical baseline.
Help me de-risk this software project before we start building.
Ask me the minimum useful questions before recommending an architecture direction.

⸻

Design Philosophy

This workflow is intentionally lightweight.

It should not feel like:

* A formal intake form
* A requirements-gathering marathon
* A stakeholder survey
* A premature architecture review
* A consulting questionnaire

It should feel like a short conversation that helps the user clarify what matters before making technical decisions.

The assistant should optimize for forward motion, not perfect information.

⸻

Usage Notes

Keep It Conversational

The assistant should not expose internal state names, validation rules, or finite state machine mechanics.

The user should only experience a smooth three-question conversation.

Avoid Over-Clarifying

The assistant may ask one lightweight clarification per stage, but should not get stuck trying to force perfect answers.

If the user remains vague, the assistant should proceed with a reasonable assumption and flag it in the final baseline.

Do Not Jump to Tech Too Early

The assistant should avoid recommending frameworks, databases, infrastructure, or implementation details before the three discovery areas are complete.

Architecture recommendations should come after the pain, tradeoff, and risk are understood.

Prefer Actionable Synthesis

The final baseline should help the user decide what to do next.

Good next steps include:

* Define an MVP slice
* Map the current workflow
* Draft a system diagram
* Run a technical spike
* Audit data quality
* Identify integration dependencies
* Prototype the riskiest workflow
* Align stakeholders on the tradeoff

⸻

Example Session

User:

Help me scope a new internal tool.

Assistant:

I’ll keep this lightweight. I’ll ask three quick questions to understand the pain, the tradeoff, and the biggest risk — then I’ll turn that into a simple project baseline.
Imagine this project works beautifully. What annoying, expensive, slow, or frustrating thing has mostly disappeared for your team or users?

User:

Our account managers no longer have to manually pull updates from five systems before customer calls.

Assistant:

If things get harder than expected, what has the most room to move: scope, budget, or timeline?

User:

Scope. We need something useful quickly, even if it starts small.

Assistant:

What is the thing people may not want to say out loud, but that could quietly derail this if we ignore it?

User:

The data is messy and no one fully agrees which system is the source of truth.

Assistant:

## Project Baseline Document
### Core Pain to Remove
Account managers are spending too much time manually gathering customer context from multiple systems before calls.
### Likely Shape of the Project
This should likely start as a focused workflow consolidation tool optimized for speed, clarity, and immediate usefulness rather than broad platform coverage.
### Flex Point
Scope is the main flex point. The architecture should support a thin MVP slice first, with room to add more systems and workflows later.
### Main Risk to Design Around
The primary risk is messy data and unclear source-of-truth ownership. The project should not assume clean, unified data at the start.
### Tension Check
There is a mild tension between the desire for quick usefulness and the unresolved data ownership issue. The MVP should avoid pretending to solve all data consistency problems upfront.
### Open Assumptions
No major assumptions.
### Recommended Next Step
Map the current pre-call workflow and identify the smallest useful customer summary that can be generated from one or two trusted systems first.

⸻

Maintenance Notes

Update SKILL.md if the workflow should become:

* More lightweight
* More rigorous
* More technical
* More stakeholder-oriented
* More suitable for agencies, internal teams, or product managers

When editing, preserve the core three-question structure unless there is a strong reason to expand it.

The most important design constraint is maintaining low friction while still surfacing enough signal to guide useful technical planning.

⸻

License

Use, adapt, and modify this workflow for internal or client-facing project discovery.
