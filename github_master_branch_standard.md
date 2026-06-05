# GitHub Master Branch Standard

- repository SSH remote: git@github.com:shiweit-cyber/firecad-auto-drawing.git
- repository web URL: https://github.com/shiweit-cyber/firecad-auto-drawing
- official branch: master
- main branch status: not used

## Required Git Commands

- normal pull: git pull --rebase origin master
- normal push: git push origin master
- do not run git push origin main unless a main branch is explicitly created and approved
- do not create main automatically
- do not force push
- do not make the repository public

## ChatGPT Read Rule

ChatGPT should read official handoff files from origin/master:

- 04_AI交接/node_reports/
- 04_AI交接/status/
- 04_AI交接/tasks_pending/
- 04_AI交接/tasks_done/
- 04_AI交接/tasks_blocked/
- 04_AI交接/gpt_brain/

If ChatGPT cannot read those files, Tang boss should confirm that the ChatGPT GitHub Connector / Codex authorization includes repository shiweit-cyber/firecad-auto-drawing.

## Safety

- do not commit secrets, tokens, passwords, or SSH private keys
- do not commit real customer DWG/DXF
- do not open the repository to public access automatically
- do not force push
