# Re-design Task Prompt

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
- Review the code in the aforementioned Code Locations section in preparation for later steps


### (Step 2)
Spawn a new general purpose subagent to do the following:
- Retrieve the latest copy of the Claude Design project specified by the user in preparation for later steps


### (Step 3)
Spawn a new general purpose subagent to do the following:
- Revew the the current system design doc in ./docs/current-design.md in preparation for later steps


### (Step 4)
Spawn a new general purpose subagent to do the following:
- Revew the the current system design delta doc in ./docs/design-delta.md in preparation for later steps 


### (Step 5)
Spawn a new general purpose subagent to do the following:
- Revew the the current design delta implementation plan doc in ./docs/plan.md in preparation for later steps


### (Step 6)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the updated/changed features requested by the user
- Review results of (Step 1), (Step 2), (Step 3), (Step 4) and (Step 5) 
- Update the ./docs/current-design.md based on the updated/changed features requested by the user using the results of previous steps, concise verbiage and plenty of mermaid diagrams for architecture and sequences
- Output an overview of all changes to the ./docs/current-design.md for the user to review.
- Request the user's sign-off, or further requests for updates/changes, on the current-design.md before procceeding to (Step 7).


### (Step 7)
Spawn a new general purpose subagent to do the following:
- Review the results of (Step 6)
- Commit and push all changes


### (Step 8)
- Delete ./docs/design-delta.md
- Delete ./docs/plan.md
- Commit and push the changes


### (Step 9)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 1) and (Step 2)
- Review the updated ./docs/current-design.md doc commited in (Step 7)
- Review the user's list of new, updated and/or changed features they'd like to see designed, and determine how it relates to the existing code from (Step 1), and the latest copy of the Claude Design project (Step 2) and the current-design.md doc
- Document the new, proposed system design delta necessary to update the current system design with the requested new features specificed by the user in ./docs/design-delta.md with concise verbiage and plenty of mermaid diagrams for architecture and sequences 
- Request the user to review the ./docs/design-delta.md and approve before proceeding to (Step 10)


### (Step 10)
Spawn a new general purpose subagent to do the following:
- Review the results of (Step 9)
- Commit and push all changes


### (Step 11)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 1) and (Step 2)
- Review the updated ./docs/current-design.md doc commited in (Step 7)
- Review the ./docs/design-delta.md doc commited in (Step 10)
- Document a new, proposed test-driven-development implementation plan that consists of an ordered, numbered, table of tasks (with Stagehand e2e tests for UI, non-UI e2e tests elsewhere, and unit test everywhere) necessary to implement the proposed system design delta in ./docs/plan.md 
- Request the user to review the ./docs/plan.md and approve before proceeding to (Step 12)


### (Step 12)
Spawn a new general purpose subagent to do the following:
- Review the results of (Step 11)
- Commit and push all changes


### (Step 13)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 6), (Step 9) and (Step 11)
- Propose any recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents.


### (Step 14)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 6), (Step 9) and (Step 11)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 13) are valid.


### (Step 15)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 6), (Step 9) and (Step 11)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 13) are necessary.


### (Step 16)
Spawn a new general purpose subagent to do the following:
- Review the results of from (Step 14) and (Step 15)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 13) were deemed to be both valid and necessary in (Step 14) and (Step 15), respectively.
- If any of the recommended revisions from (Step 13) were deemed to be both valid and necessary, proceed to (Step 17). Otherwise, skip (Step 17)


### (Step 17)
Spawn a new fabulous-tech-lead subagent to do the following:
- Implement the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 6) which were deemed to be both valid and necessary in (Step 9)
- Commit and push all changes
