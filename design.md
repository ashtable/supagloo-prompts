# Design Task Prompt

## Code Locations:
- Supagloo Prompts: ~/code/supagloo-prompts (Git submodule in all other projects)
- Supagloo Docker Compose: ~/code/supagloo (has all dependency projects as submodules)
- Supagloo Prisma & Zod Types: ~/code/supagloo-database-lib (handles migrations, exports types for other projects)
- Supagloo Next.js UI: ~/code/supagloo-nextjs
- Supagloo Node.js API: ~/code/supagloo-nodejs-api
- Supagloo Node.js DBOS Workflows: ~/code/supagloo-nodejs-dbos

## Code Locations:

### Prompts for Local Development
- Supagloo Prompts: ~/code/supagloo-prompts (should be a Git submodule in all other projects)

### Docker Compose for Local Development
- Supagloo Docker Compose: ~/code/supagloo (should have all dependency projects from compose yaml file as submodules)

### Database Migrations & Data Types
- Supagloo Prisma & Zod Types: ~/code/supagloo-database-lib (handles migrations, exports types for other projects and should be a a Git submodule in the UI, API and Durable Execution Layer projects)

### UI w/ Dockerfile IaC
- Supagloo Next.js UI: ~/code/supagloo-nextjs
- Deployed to Railway (CI/CD setup and site live at https://supagloo.com/)

### API w/ Dockerfile IaC
- Supagloo Node.js API: ~/code/supagloo-nodejs-api
- Deploy to Railway (manual CI/CD setup not yet completed)

### Durable Execution Layer w/ Dockerfile IaC
- Supagloo Node.js DBOS Workflows: ~/code/supagloo-nodejs-dbos
- Deploy to Railway (manual CI/CD setup not yet completed)

## Instructions
Run the following steps exactly as specified without any deviations:


### (Step 1)
Spawn a new general purpose subagent to do the following:
- Review the code in the aforementioned Code Locations section
- Review the user's list of new features they'd like to see designed, and determine how it relates to the existing code since we need that info for (Step 3)


### (Step 2)
Spawn a new general purpose subagent to do the following:
- Review the Claude Design project specified by the user
- Review the user's list of new features they'd like to see designed, and determine how it relates to the Claude Design project since we need that info for (Step 3)


### (Step 3)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 1) and (Step 2)
- Document the current system's design in ./docs/current-design.md with concise verbiage and plenty of mermaid diagrams for architecture and sequences (create directory if necessary, and then delete the file if it already exists).
- Document the new, proposed system design delta necessary to update the current system design with the requested new features specificed by the user in ./docs/design-delta.md with concise verbiage and plenty of mermaid diagrams for architecture and sequences (create directory if necessary, and delete the file if it already exists).
- Document a new, proposed test-driven-development implementation plan that consists of an ordered, numbered, table of tasks (with Stagehand e2e tests for UI, non-UI e2e tests elsewhere, and unit test everywhere) necessary to implement the proposed system design delta in ./docs/plan.md (create directory if necessary, and delete the file if it already exists).


### (Step 4)
Spawn a new general purpose subagent to do the following:
- Review the results of (Step 3)
- Commit and push all changes


### (Step 5)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 1), (Step 2) and (Step 3)
- Propose any recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents


### (Step 6)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 3) and (Step 5)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 5) are valid.


### (Step 7)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 3) and (Step 5)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 5) are necessary.


### (Step 8)
Spawn a new general purpose subagent to do the following:
- Review the results of from (Step 6) and (Step 7)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 5) were deemed to be both valid and necessary in (Step 6) and (Step 7), respectively.
- If any of the recommended revisions from (Step 5) were deemed to be both valid and necessary, proceed to (Step 9). Otherwise, skip ahead to (Step 10)


### (Step 9)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 8)
- Implement the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 5) which were deemed to be both valid and necessary in (Step 8)

### (Step 10)
Spawn a new general purpose subagent to do the following:
- Review all changes
- Commit and push all changes
