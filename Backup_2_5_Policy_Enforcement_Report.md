# Backup 2.5 Policy Enforcement Report

- status: OK
- policy: 2.5 backup strategy
- main repository: private GitHub repository for code, scripts, docs, tests, and tags
- Windows local copy: AutoCAD / Tianzheng / real environment integration copy
- Mac local copy: development, dispatch, and basic test copy
- public status mirror: status reports and next tasks only
- sensitive tracked files: none found
- blocked content: DWG/DXF, PDF, Excel, archives, customer data, Tianzheng drawings, secrets
- check script: 01_代码/scripts/check_sensitive_git_files.ps1
- automation integration: Windows guard records a non-blocking summary each cycle; FAILED check stops commit
