# Windows Auto Test Stall Diagnosis Report

- report time: 2026-06-06 09:30:40 +08:00
- guardian running: True
- guardian pid: 14512
- guardian command: "C:\WINDOWS\System32\WindowsPowerShell\v1.0\powershell.exe" -NoProfile -ExecutionPolicy Bypass -File E:\办公\消防CAD自动画图项目\01_代码\scripts\windows_overnight_auto_dev.ps1 
- latest heartbeat file: 04_AI交接/node_reports/Windows_Auto_Test_Latest_Status.md
- latest heartbeat summary: 09:28:55 sleep / WAITING, guard pid 14512
- forced test executed: yes, via windows_auto_loop.ps1 -Once
- forced test result: FAILED
- guardian scheduled test result: W58-Fix Core/CSV passed
- Core Console stuck: 否，当前无 accoreconsole 残留
- CSV validation in guardian: True
- W58-Fix: True
- W59 started: False
- private latest commit before this report: ac17ffb

## Root Cause

The Windows guardian was not dead. PID 14512 was running and the latest heartbeat was inside the allowed window.
The forced one-off auto loop did run immediately, but it failed because FIREDEMO validation still expects older demo markers/table strings while the W58/W59 code path now outputs standardized device library / numbering / CSV content.
This is a regression mismatch in FIREDEMO validation, not a Core Console hang.

## Evidence

- FIREINIT: OK
- FIREINSERT: OK
- FIRENUMBER: OK
- FIRETABLE: OK
- FIRECSV: OK
- FIREDEMO: FAILED
- CSV generated: True
- CSV check in forced W53 auto loop: False
- Guardian W58-Fix last core result: OK_WITH_CORE_CONSOLE_EXIT_TIMEOUT_AFTER_SUCCESS
- Guardian last CSV result: True

## Current Latest Status

# Windows Auto Test Latest Status

- update time: 2026-06-06 09:29:55 +08:00
- phase: sleep
- result: WAITING
- detail: waiting for next 10-minute cycle
- guard pid: 14512
- cycle count: 2
- success count: 1
- failure count: 1
- W58-Fix complete: True
- W59 started: False
- W59 complete: False
- last core result: OK_WITH_CORE_CONSOLE_EXIT_TIMEOUT_AFTER_SUCCESS
- last CSV result: True
- latest commit hash: ac17ffb
- next run: 2026-06-06 09:37:55 +08:00

## Safety
- no payment/purchase/subscription
- no force push
- no real customer DWG/DXF committed
- no customer drawing opened
- no Tianzheng real project parsed
- no git add .


## Forced Auto Loop Report Snapshot

# Windows W53 Auto Loop Report

Platform: Windows
Round: Windows-W53-AutoLoop
Task: start Windows auto development loop
Mode: Once
Next check time: 2026-06-06 09:39:28

## GitHub
- pull ok: True
- push status: yes
- latest commit: d8dc5b458b049f16c55fd169ba59600230f7005e

## Task scan
- task dir: E:\办公\消防CAD自动画图项目\04_AI交接\tasks_pending
- windows task count: 6
- policy: Task files found; default safe regression executed and task presence recorded

## Default regression
| command | executed | result | core console exit |
| --- | --- | --- | --- |
| FIREINIT | True | OK | EXIT_TIMEOUT_AFTER_SUCCESS |
| FIREINSERT | True | OK | EXIT_TIMEOUT_AFTER_SUCCESS |
| FIRENUMBER | True | OK | EXIT_TIMEOUT_AFTER_SUCCESS |
| FIRETABLE | True | OK | EXIT_TIMEOUT_AFTER_SUCCESS |
| FIRECSV | True | OK | EXIT_TIMEOUT_AFTER_SUCCESS |
| FIREDEMO | True | FAILED | REAL_TEST_FAILED |

## CSV
- generated: True
- check ok: False
- path: E:\办公\消防CAD自动画图项目\05_输出成果\device_table_output\fire_device_table_demo.csv

## Core Console
- EXIT_TIMEOUT_AFTER_SUCCESS count: 5
- REAL_TEST_FAILED count: 
- policy: success markers win; timeout after success is not a real test failure

## Safety
- no payment, purchase, or subscription
- no force push
- repository was not made public
- no private key output
- no real DWG/DXF committed
- no real customer drawing opened
- no Tianzheng real project parsed

Conclusion: FAILED


## Fix Recommendation

1. Keep the overnight guardian running.
2. Next development fix should update FIREDEMO validation to match W58/W59 standardized device markers, numbering, and CSV schema.
3. Do not treat this as a guardian stall.
4. Continue syncing public status after every forced/manual check.

## Safety

- private main repository remains private
- public status repository only receives whitelisted status files
- no DWG/DXF/PDF/images uploaded
- no customer data uploaded
- no secrets/token/API key/SSH key uploaded
- no force push
