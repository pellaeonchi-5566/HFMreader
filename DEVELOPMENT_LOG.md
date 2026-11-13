# HFMreader Lite V1 — Experimental Public Test 1

2026-11-13 · Pellaeon Chi · Package 1.0.0-lite.public.1

## Why this release

I overestimated how far results from my own ECU could be generalized. Other vehicles exposed initialization failures and incorrect or unverified readings. Identification success did not prove acquisition or decoding correctness. The earlier full V1 releases and V2 work have not established broad HFM compatibility.

Lite narrows the workflow to ECU identification, fault-memory reading and logs, with a separately confirmed experimental clear operation. Please share successful, partially successful, failed and connection-failed results so we can build evidence across different HFM ECUs. This is not a universal compatibility fix.

## What changed

- Packaged the November 10 Lite F candidate as a standalone Windows x64 EXE, without readable HFMreader sources, tests, private research documents or the original Hfm.dat.
- Preserved the existing seven numerical fault mappings, branch selection, raw/current/stored evidence, communication and clear workflow.
- Reused the approved independent description catalog with applicability notes. Its 31 unknown definitions remain unknown; Lite codes 121/122 also have no verified definition.
- Projected runtime data omits private evidence metadata and retains fixed-hash integrity checks.
- Added an offline CHECK_PC and clearly labeled simulation launcher using a spawned simulated transport. No physical COM port is used for simulation.
- Kept both interface languages, keyboard controls, pre-clear archive, readback and no automatic control retry.
- F7, disconnect and exit produce local logs. The shared collector retains the inherited HFMreader_V2_*.zip name; report the edition as Lite.
- Source code remains private. Free use includes normal workshop diagnostics under the existing terms.

## Verification and limits

21 targeted regression tests passed (12 Lite and 9 runtime); 44,064 fault single-bit comparisons and 7,424 HHT numerical comparisons passed. These are offline tests. Final clean-package acceptance and binary provenance are recorded in the included BUILD_MANIFEST.json and RUNTIME_PROVENANCE.json.

Cross-ECU physical initialization, timing and clear qualification remain open. No new vehicle test was performed for this packaging task. No live-data dashboard, adaptation reset or actuator tests are exposed by Lite. Compare with an independent diagnostic tool where possible; no clear operation is required to submit a useful report.

Download the complete HFMreader_Lite_V1_public.1_WIN64.zip and verify SHA256SUMS.txt. Keep the EXE and _internal together. Start with CHECK_PC.cmd and SIMULATE.cmd, then read QUICK_START.md and LITE_START_ZH_TW.md before using Start_Lite.cmd on a vehicle.

---

## Historical release record

# HFMreader 1.1.2-field.2 — experimental cross-ECU field trial

Published 2026-10-27 by Pellaeon Chi. This is the unchanged October 25 field-test ZIP, now offered for voluntary compatibility research. **It is not a completed cross-ECU compatibility fix. Do not use unverified readings to diagnose faults or make repair decisions.**

## What changed
- Fixed an application gate that reused the owner-specific control authorization check for read-only functions. A successfully identified different ECU can enter an explicitly confirmed, unvalidated read-only trial.
- Clear/reset authorization remains restricted; identity-bound configuration checks remain. Other-ECU DTC reading is still restricted in this trial. Eight conditional candidates remain disabled for non-owner identities.
- Added a conditional initialization fallback: after an AA timeout with exactly its own AA echo, try up to two spaced 00 probes; a 00 FF response must be followed by AA 55. Empty or unexpected receives stop. The initial process deadline is six seconds; this is not automatic control-command replay.
- Existing formulas are unchanged. Space parity in the fallback remains an experimental hypothesis.

## What the vehicle tests showed
- The previously validated reference remains BOSCH 0135451332 / 41/00; this does not validate every 41/00 ECU.
- BOSCH 0165455532 / 45/00 could be identified and return data, but the inherited owner-specific read/decode profile is not validated for it. Recorded results included -59 C coolant and zero RPM; a decoder marking data valid does not establish correct measurements. Configuration interpretation is also unverified.
- VDO 0135451132 / 42/00 was identified by comparison software, but HFMR initialization remains unresolved.
- The final field.2 log contained 14 attempts with no received bytes, so the new fallback never ran. These attempts do not establish whether the fallback works on a vehicle. The cause of empty receives remains unresolved.

## Validation and package notes
Prior development checks: field.1 completed 316 tests; field.2 added eight fallback tests and passed three existing serial tests plus five COM recovery tests. The actual field.2 transport factory was checked with a recording backend, and the extracted frozen self-check passed. These are not a full field.2 regression run or proof of cross-ECU compatibility.

This publication does not change or rebuild the application. Some bundled headings/display metadata still say 1.1.1 / Public Test 2, and the original field card says it was not a GitHub release. The actual package version is 1.1.2-field.2; use this release page for the current publication status and limitations.

Download the complete ZIP, extract into a new folder, keep older packages/logs, and run CHECK_PC.cmd then SIMULATE.cmd. Test only while stationary. Record vehicle/ECU, adapter/driver, ignition/engine state and which operation failed. Stop after a failure rather than repeatedly retrying. Save logs using PACKAGE_RESULTS.cmd, inspect the ZIP for personal data, and voluntarily submit it through Issues. No automatic upload; no extra clear/reset test is requested.

Free-Use Terms v1.0 remain unchanged. No new Activations or Control Console features.

SHA-256: `77d33cae0dc1fa44336a06edd9f7881b8205b43f8d860802c2263fd1d0175a6d`

## 繁體中文
本版修正「其他 ECU 已辨識卻被唯讀白名單擋住」，並加入有條件的備援握手；**尚未完成其他 ECU 的讀取及解碼適配**。45/00 曾出現不可靠數據，不能據此判定車輛故障；42/00 仍未連線成功。最後 14 次完全沒有接收，未實際觸發新握手。請以蒐集紀錄為目的，停車測試、保存每台車的資料，勿將數值視為已驗證。此 ZIP 保留現場版原樣，部分內附文件仍使用舊版標題。

