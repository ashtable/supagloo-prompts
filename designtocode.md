# Coding Task Prompt to Convert Designed Task to Code

## Design Doc Locations:

### Current System Design Doc 
- ./docs/current-design.md


### Design Delta Doc 
- ./docs/design-delta.md


### Implementation Plan Doc
- ./docs/plan.md


## Code Locations:

### Prompts for Local Development
- Supagloo Prompts: ~/code/supagloo-prompts (Git submodule in all other projects)
- Not deployed anywhere.


### Docker Compose for Local Development
- Supagloo Docker Compose: ~/code/supagloo (has all dependency projects as submodules)
- Also referred to as "root" and "supagloo" in the design docs.
- Not deployed anywhere, only for local development.


### Database Migrations & Data Types
- Supagloo Prisma & Zod Types: ~/code/supagloo-database-lib (handles migrations, exports types for other projects)
- Git submodule in the UI, API and Durable Execution layer projects
- Also referred to as "db-lib" and "supagloo-database-lib" in the design docs.


### UI w/ Dockerfile IaC
- Supagloo Next.js UI: ~/code/supagloo-nextjs
- Also referred to as "nextjs" and "supagloo-nextjs" in the design docs.
- Deployed to a Railway project with Postgres and a Railway, S3-Compatible Bucket


### API w/ Dockerfile IaC
- Supagloo Node.js API: ~/code/supagloo-nodejs-api
- Also referred to as "api" and "supagloo-nodejs-api" in the design docs.
- Will be deployed to the same Railway project as the UI, Postgres and Railway, S3-Compatible Bucket.


### Durable Execution Layer w/ Dockerfile IaC
- Supagloo Node.js DBOS Workflows: ~/code/supagloo-nodejs-dbos
- Also referred to as "dbos" and "supagloo-nodejs-dbos" in the design docs.
- Will be deployed to the same Railway project as the UI, Postgres and Railwway, S3-Compatible Bucket.


## Instructions
Run the following steps exactly as specified without any deviations:


### (Step 1)
Spawn a new general purpose subagent to do the following:
- Review the "Task table" in the Implementation Plan in ./docs/plan.md to identify the next, incomplete software engineering task, and then designate that to be the Current Software Engineering Task in preparation for (Step 2), (Step 3), (Step 4), (Step 5), (Step 6), (Step 13) and (Step 14)


### (Step 2)
Spawn a new general purpose subagent to do the following:
- Review the Current Software Engineering Task from (Step 1).
- Review current system's design in ./docs/current-design.md and identify the portions relevant to the current software engineering task in preparation for (Step 6)


### (Step 3)
Spawn a new general purpose subagent to do the following:
- Review the Current Software Engineering Task from (Step 1).
- Review the proposed system design delta in the ./docs/design-delta.md and identify the portions relevant to the current software engineering task in preparation for (Step 6).


### (Step 4)
Spawn a new general purpose subagent to do the following:
- Review the Current Software Engineering Task from (Step 1).
- Review the proposed system design delta in the Claude Design project (as applicable only, likely just for UI tasks) and identify the portions relevant to the current software engineering task in preparation for (Step 6).


### (Step 5)
Spawn a new general purpose subagent to do the following:
- Review the Current Software Engineering Task from (Step 1).
- Review the code in the aforementioned "Code Locations" section that's relevant to the current software engineering task in preparation for (Step 6).


### (Step 6)
Spawn a new tech-lead subagent to do the following:
- Review the Current Software Engineering Task from (Step 1).
- Review the results from (Step 2), (Step 3), (Step 4), and (Step 5) 
- Document a detailed, test-driven development plan for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task). Ensure that this tdd plan starts with the appropriate end-to-end tests and unit tests (for Stagehand tests use act/extract/observe whenever possible, use the agent with Gloo AI endpoints for the OpenAI calls only when necessary for complex UI workflows, and avoid brittle UI unit tests that would cover features being exercised by Stagehand tests).
- Review and implement the integration tests and unit tests for the current task in the aforementioned Code Locations using the detailed, test-driven development plan in (Step 6) in ./scratch/name-of-current-task.md (with the appropriate file name for each task).
- Run the tests and ensure that they are all Red (i.e., failing)
- Explain to user which tests were written, and what functionality needs to be implemented to make the tests turn Green (i.e., passing)
- Implement the code for the current task in the aforementioned Code Locations using the test-driven development plan in (Step 6) in ./scratch/name-of-current-task.md (with the appropriate file name for each task)
- Ensure that all of the tests are now Green (i.e., passing)


### (Step 7) 
Spawn a general purpose subagent to do the following:
- Review the code written in (Step 6) across all the aforementioned Code Locations
- Commit and push all changes
- Review the detailed, test-driven development plan from (Step 6) for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task).
- Perform a code review of the work completed in (Step 6) across all the aforementioned Code Locations against the detailed, test-driven development plan.
- Suggest any recommended revisions to the work completed in (Step 6) 


## (Step 8)
Spawn a new general purpose subagent to do the following:
- Review the detailed, test-driven development plan from (Step 6) for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task).
- Review the recommended revisions from (Step 7)
- Determine which of the recommended revisions from (Step 7) are valid


## (Step 9)
Spawn a new general purpose subagent to do the following:
- Review the detailed, test-driven development plan from (Step 6) for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task).
- Review the recommended revisions from (Step 7)
- Determine which of the recommended revisions from (Step 7) are necessary



#### (Step 10)
Spawn a new general purpose subagent to do the following:
- Determine if any of the recommended revisions from (Step 7) were independently deemed to be both valid in (Step 8) and necessary in (Step 9). If so, explain the changes that need to be made to the user, and then proceed to (Step 11) without waiting for permission. If not, skip ahead to (Step 13)


### (Step 11)
Spawn a new tech-lead subagent to do the following:
- Implement the recommended revisions that were deemed to be both valid and necessary in (Step 10) across all the aforementioned Code Locations 
- Ensure that all tests are Green (i.e., passing).


#### (Step 12) 
Spawn a new general purpose subagent to do the following:
- Review the code written in (Step 11) across all the aforementioned Code Locations
- Commit and push all changes


### (Step 13)
Spawn a new general purpose subagent to do the following:
- In each of the aforementioned Code Locations that were impacted, run the "/release" command/skill to merge the changes into main, then bump the submodule pointer in all parent repos and fast-forward the submodule copy in each parent repo. 
- Review the Current Software Engineering Task from (Step 1).
- Mark the current task as "Done" by adding the text " (Done!)" to the "#" column of the "Task table" in the ./docs/plan.md file 
- Commit and push the change to ./docs/plan.md


### (Step 14)
Spawn a new general purpose subagent to do the following:
- Review the Current Software Engineering Task from (Step 1).
- Review the code written in (Step 6) and (Step 11), as well as the releases/submodule pointer bumps from (Step 12), and then provide a detailed briefing to the user of what work was completed.
