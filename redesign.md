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
- Revew the the current design delta implementation plan doc in ./docs/plan.md in preparation for later steps (in particular, note which of the tasks have been completed, and the number of the Last Completed Task)


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
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 1), (Step 2) and (Step 5)
- Review the updated ./docs/current-design.md doc commited in (Step 7)
- Review which of the tasks from the implementation plan in ./docs/plan.md have already been completed, and which have not
- Review the user's list of new, updated and/or changed features they'd like to see designed, and determine how it relates to the existing code from (Step 1), the latest copy of the Claude Design project (Step 2) and the updated ./docs/current-design.md doc
- Update the ./docs/design-delta.md file with the new, proposed system design delta necessary to update the current system design documented in ./docs/current-design.md with the new updates/changes to features now-requested by the user, as well as the previously-specificed tasks that have not yet been implemented in ./docs/plan.md, with concise verbiage and plenty of mermaid diagrams for architecture and sequences (for clarity, make sure that this document acknolwedges that part of the system was designed, and now we're updating the design based on updated requirements)
- Request the user to review the ./docs/design-delta.md and approve before proceeding to (Step 9)


### (Step 9)
Spawn a new general purpose subagent to do the following:
- Review the results of (Step 8)
- Commit and push all changes


### (Step 10)
Spawn a new fabulous-tech-lead subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 5)
- Review the updated ./docs/current-design.md doc commited in (Step 7)
- Review which of the tasks from the implementation plan in ./docs/plan.md have already been completed, and which have not 
- Review the updated ./docs/design-delta.md doc commited in (Step 9)
- Update the ./docs/plan.md document's pre-existing table of tasks with additional emergency tasks (with Stagehand e2e tests for UI, non-UI e2e tests elsewhere, and unit test everywhere) necessary to implement the proposed system design delta in ./docs/design-delta.md 
- For example, let's say that the we find that task "34" was the Last Completed Task in the tasks table of ./docs/plan.md in (Step 5). All emergency tasks should be numbered using scheme of "34-E1", "34-E2", "34-E3", and so on. The emergency tasks should be followed by the previously incomplete tasks. The goal is that we update the ./docs/plan.md tasks table so that we only insert new, emergency tasks after the Last Completed Task, and retain all the incomplete tasks that follow (though it's okay to update the incomplete tasks based on changes to the design with ./docs/design-delta.md overruling any pre-existing, incomplete tasks in ./docs/plan.md)
- Request the user to review the ./docs/plan.md and approve before proceeding to (Step 11)


### (Step 11)
Spawn a new general purpose subagent to do the following:
- Review the results of (Step 10)
- Commit and push all changes


### (Step 12)
Spawn a new tech-lead subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 6), (Step 8) and (Step 10)
- Propose any recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents.


### (Step 13)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 6), (Step 8) and (Step 10)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 12) are valid.


### (Step 14)
Spawn a new general purpose subagent to do the following:
- Review the results from (Step 1), (Step 2), (Step 6), (Step 8) and (Step 10)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 12) are necessary.


### (Step 15)
Spawn a new general purpose subagent to do the following:
- Review the results of from (Step 13) and (Step 14)
- Determine which of the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 12) were deemed to be both valid and necessary in (Step 13) and (Step 14), respectively.
- If any of the recommended revisions from (Step 12) were deemed to be both valid and necessary, proceed to (Step 16). Otherwise, skip (Step 16) and (Step 17)


### (Step 16)
Spawn a new fabulous-tech-lead subagent to do the following:
- Implement the recommended revisions to the ./docs/current-design.md, ./docs/design-delta.md and ./docs/plan.md documents from (Step 12) which were deemed to be both valid and necessary in (Step 15)

### (Step 17)
Spawn a new general purpose subagent to do the following:
- Review the changes from (Step 16)
- Commit and push all changes
