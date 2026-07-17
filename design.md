# Design Task Prompt

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
- Document the current system's design in ./docs/current-design.md with concise verbiage and plenty of mermaid diagrams for architecture and sequences (create directory if necessary, and then delete the file if it already exists).
- Request the user to review the ./docs/current-design.md and approve before proceeding to (Step 4)


### (Step 2)
Spawn a new general purpose subagent to do the following:
- Retrieve the latest copy of the Claude Design project specified by the user


### (Step 3)
Spawn a new tech-lead subagent to do the following:
- Review the results from (Step 1) and (Step 2)
- Review the user's list of new features they'd like to see designed, and determine how it relates to the existing code from (Step 1), and the latest copy of the Claude Design project (Step 2)
- Document the new, proposed system design delta necessary to update the current system design with the requested new features specificed by the user in ./docs/design-delta.md with concise verbiage and plenty of mermaid diagrams for architecture and sequences (create directory if necessary, and delete the file if it already exists).
- Request the user to review the ./docs/design-delta.md and approve before proceeding to (Step 4)


### (Step 4)
Spawn a new general purpose subagent to do the following:
- Review the results of (Step 3)
- Commit and push all changes


### (Step 5)
Spawn a new tech-lead subagent to do the following:
- Review the results from (Step 1), (Step 2) and (Step 3)
- Document a new, proposed test-driven-development implementation plan that consists of an ordered, numbered, table of tasks (with Stagehand e2e tests for UI, non-UI e2e tests elsewhere, and unit test everywhere) necessary to implement the proposed system design delta in ./docs/plan.md (create directory if necessary, and delete the file if it already exists).
- Request the user to review the ./docs/plan.md and approve before proceeding to (Step 6)


### (Step 6)
Spawn a new tech-lead subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 3) and (Step 5)
- Propose any recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents.


### (Step 7)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 3) and (Step 5)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 6) are valid.


### (Step 8)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 3) and (Step 5)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 6) are necessary.


### (Step 9)
Spawn a new tech-lead subagent to do the following:
- Review the results of from (Step 7) and (Step 8)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 6) were deemed to be both valid and necessary in (Step 7) and (Step 8), respectively.
- If any of the recommended revisions from (Step 6) were deemed to be both valid and necessary, proceed to (Step 10). Otherwise, skip (Step 10)


### (Step 10)
Spawn a new tech-lead subagent to do the following:
- Implement the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 6) which were deemed to be both valid and necessary in (Step 9)
- Commit and push all changes
