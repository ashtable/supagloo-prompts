# Design

## Scope


## Code Locations:
- Supagloo Prompts: ~/code/supagloo-prompts (Git submodule in all other projects)
- Supagloo Docker Compose: ~/code/supagloo (has all dependency projects as submodules)
- Supagloo Prisma & Zod Types: ~/code/supagloo-database-lib (handles migrations, exports types for other projects)
- Supagloo Next.js UI: ~/code/supagloo-nextjs
- Supagloo Node.js API: ~/code/supagloo-nodejs-api
- Supagloo Node.js DBOS Workflows: ~/code/supagloo-nodejs-dbos

## Instructions
Run the following steps exactly as specified without any deviations:

### (Step 1)
Turn on planning mode.

### (Step 2)
Spawn a new general purpose subagent to do the following:
- Review the code in the aforementioned Code Locations section

### (Step 3)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the context from (Step 2)
- Document the current system's design in ../docs/current-design.md with concise verbiage and plenty of mermaid diagrams for architecture and sequences (create directory if necessary, and then delete the file if it already exists).
- Document the new, proposed system design delta necessary to update the current system design with the requested new features specificed by the user in ../docs/design-delta.md with concise verbiage and plenty of mermaid diagrams for architecture and sequences (create directory if necessary, and delete the file if it already exists).
- Document a new, proposed implementation plan that consists of a numbered, table of high-level tasks (including necessary details for a Claude Code agent) necessary to implement the proposed system design delta in ../docs/plan.md 

### Step 4 
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the context from (Step 2)
- Review the context from (Step 3)
- Propose any recommended revisions to the ../docs/current-design.md, ../docs/design-delta.md and ../docs/plan.md documents

### Step 5 
Spawn a new general purpose subagent to do the following:
- Review the context from (Step 2)
- Review the context from (Step 3)
- Review the context from (Step 4)
- Determine which of the recommended revisions to the ../docs/current-design.md, ../docs/design-delta.md and ../docs/plan.md documents from (Step 4) are valid

### Step 6 
Spawn a new general purpose subagent to do the following:
- Review the context from (Step 2)
- Review the context from (Step 3)
- Review the context from (Step 4)
- Determine which of the recommended revisions to the ../docs/current-design.md, ../docs/design-delta.md and ../docs/plan.md documents from (Step 4) are necessary

### Step 7 
Spawn a new general purpose subagent to do the following:
- Review the context from (Step 5)
- Review the context from (Step 6)
- Determine which of the recommended revisions to the ../docs/current-design.md, ../docs/design-delta.md and ../docs/plan.md documents from (Step 4) were deemed to be both valid and necessary
- If any of the recommended revisions from (Step 4) were deemed to be both valid and necessary, proceed to (Step 8). Otherwise, skip ahead to (Step 12)

### Step 8 
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the context from (Step 7)
- Implement the recommended revisions to the ../docs/current-design.md, ../docs/design-delta.md and ../docs/plan.md documents from (Step 4) which were deemed to be both valid and necessary in (Step 7)

### Step 9 
Spawn a new general purpose subagent to do the following:
- Commit and push all changes
