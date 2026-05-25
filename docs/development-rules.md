\# Development Rules



\## General Rules



1\. Work in small changes.

2\. Commit after each stable change.

3\. Review git diff before every commit.

4\. Do not add dependencies casually.

5\. Do not commit secrets.

6\. Do not use real customer data.

7\. Do not let Claude make broad changes without a narrow scope.



\## Claude Code Workflow



Use this pattern:



1\. Ask Claude to inspect.

2\. Ask Claude to propose a plan.

3\. Approve only the specific change.

4\. Review the changed files.

5\. Run tests or basic validation.

6\. Commit the change.



\## Safe Claude Prompt Pattern



Use prompts like:



"Inspect the repository and propose the smallest next step. Do not modify files yet."



Then:



"Make only the approved changes. Do not add dependencies unless necessary. Do not touch files outside the stated scope."



\## Git Workflow



Before changes:



git status



After changes:



git diff

git status

git add .

git commit -m "Describe the change clearly"

git push



\## Dependency Rules



Before adding a package, answer:



1\. Why is it needed?

2\. Is it actively maintained?

3\. Is it widely used?

4\. Does it require sensitive permissions?

5\. Is there a simpler built-in option?



\## Secret Rules



Use .env.example for placeholders.



Use .env for real local values.



Never commit .env.

