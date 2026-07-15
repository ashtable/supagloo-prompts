# Coding Task Prompt

## Code Locations:

### Prompts for Local Development
- Supagloo Prompts: ~/code/supagloo-prompts (Git submodule in all other projects)

### Docker Compose for Local Development
- Supagloo Docker Compose: ~/code/supagloo (has all dependency projects as submodules)

### Database Migrations & Data Types
- Supagloo Prisma & Zod Types: ~/code/supagloo-database-lib (handles migrations, exports types for other projects)

### UI w/ Dockerfile IaC
- Supagloo Next.js UI: ~/code/supagloo-nextjs
- Deployed to Railway

### API w/ Dockerfile IaC
- Supagloo Node.js API: ~/code/supagloo-nodejs-api
- Deploy to Railway

### Durable Execution Layer w/ Dockerfile IaC
- Supagloo Node.js DBOS Workflows: ~/code/supagloo-nodejs-dbos
- Deploy to Railway

## Instructions
Run the following steps exactly as specified without any deviations:


### (Step 1)
Run (Step 2), (Step 3), (Step 4) and (Step 5) in parallel in order to prepare the results for (Step 6)


### (Step 2)
Spawn a new general purpose subagent to do the following:
- Review the current software engineering task.
- Review current system's design in ./docs/current-design.md and identify the portions relevant to the current software engineering task for (Step 6)


### (Step 3)
Spawn a new general purpose subagent to do the following:
- Review the current software engineering task.
- Review the proposed system design delta in the ./docs/design-delta.md and identify the portions relevant to the current software engineering task for (Step 6).


### (Step 4)
Spawn a new general purpose subagent to do the following:
- Review the current software engineering task.
- Review the proposed system design delta in the Claude Design project (as applicable only) and identify the portions relevant to the current software engineering task for (Step 6).


### (Step 5)
Spawn a new general purpose subagent to do the following:
- Review the current software engineering task.
- Review the code in the aforementioned "Code Locations" section that's relevant to the current software engineering task for (Step 6).


### (Step 6)
Spawn a new tech-lead subagent to do the following:
- Review the results from (Step 2), (Step 3), (Step 4), and (Step 5) 
- Document a new, proposed test-driven development plan for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task).
- Ensure that we start with the appropriate end-to-end test in Stagehand for UI features (use act/extract/observe whenever possible, use the agent with Gloo AI endpoints for the OpenAI calls only when necessary for complex UI workflows)
- Ensure that we start with the appropriate unit tests for each piece of code that implements some logic (and avoid brittle UI unit tests that would cover features being exercised by Stagehand tests)


### (Step 7) 
Spawn a new tech-lead subagent to do the following:
- Review and implement the integration tests and unit tests for the current task from the test-driven development plan in (Step 6) in ./scratch/name-of-current-task.md (with the appropriate file name for each task).
- Run the tests and ensure that they are all Red (i.e., failing)


### (Step 8)
Spawn a new general purpose subagent to: 
- Review the specific tests that were written in (Step 7)
- Explain to user which tests were written, and what functionality needs to be implemented to make the tests turn Green (i.e., passing)
- Obtain the user's permission to proceed to (Step 9). 


### (Step 9)
Spawn a new tech-lead subagent
- As approved in (Step 8), implement the code for the features in ./scratch/name-of-current-task.md (with the appropriate file name for each task)
- Ensure that all of the tests are now Green (i.e., passing)


### (Step 10)
Spawn a general purpose subagent to do the following:
- Review the plan for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task)
- Review the work completed in (Step 7) and (Step 9), then commit and push all changes
- Suggest any recommended revisions to the work completed in (Step 7) and/or (Step 9)
- Execute (Step 11) and (Step 12) in parallel


### (Step 11) 
Spawn a new general purpose subagent to do the following:
- Review the plan for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task)
- Review the work completed in (Step 7) and (Step 9)
- Review the recommended revisions from (Step 10)
- Determine which of the recommended revisions from (Step 10) are valid


### (Step 12) 
Spawn a new general purpose subagent to do the following:
- Review the plan for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task)
- Review the work completed in (Step 7) and (Step 9)
- Review the recommended revisions from (Step 10)
- Determine which of the recommended revisions from (Step 10) are necessary


### (Step 13)
Spawn a new general purpose subagent to do the following:
- Review the recommended revisions from (Step 10)
- Determine if any of the recommended revisions from (Step 10) were deemed both valid in (Step 11) and necessary in (Step 12). If so, proceed to (Step 14). If not, skip ahead to (Step 17)


### (Step 14)
Spawn a new general purpose subagent to do the following:
- Review the plan for the current task in ./scratch/name-of-current-task.md (with the appropriate file name for each task)
- Review the tests and code written in (Step 7) and (Step 9), respectively
- Review the recommended revisions which were deemed to be both valid and necessary in (Step 13)
- Explain the changes that need to be made to the user.
- Request the user's permission to proceed to (Step 15)


### (Step 15)
Spawn a new tech-lead agent to do the following:
- As approved in (Step 14), implement the valid and necessary revisions to the tests and code 
- Ensure that all tests are Green (i.e., passing).


### (Step 16)
Spawn a new general purpose subagent to do the following:
- Commit and push all changes


### (Step 17)
Spawn a new general purpose subagent to do the following:
- If applicable, mark the current task as "Done" by adding that text to the "#" column of the corresponding task in the ./docs/plan.md file (only if applicable, ignore for pure UI changes from Claude Design).
