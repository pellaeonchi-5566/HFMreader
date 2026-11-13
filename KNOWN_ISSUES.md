# Lite known issues and research limits

- Physical cross-ECU initialization, timing and clear qualification remain open. Offline equivalence and simulation do not prove vehicle compatibility.
- Prior full builds produced wrong/unverified Bosch 45/00 values; VDO 42/00 initialization was unresolved. Lite narrows the task and collects evidence; it is not a proven fix for either problem.
- Part-number differences alone do not block a recognized HFM branch. Unknown engine identifiers retain raw-reading access where allowed, but do not acquire a guessed mapping or clear permission.
- Seven technical fault tables preserve numerical mapping. Unmapped/suppressed set bits stay visible. Partial reads remain failures, not successful empty scans.
- The independent catalog has 31 unverified descriptions plus scope-qualified definitions. Lite codes 121/122 have no verified definition in that catalog and also display `Definition not yet verified.` Do not apply an M104 reference to another engine without confirmation.
- Clear is state-changing. The previous owner-qualified sequence is retained; other recognized branches use a one-shot candidate procedure awaiting physical qualification. Pre-clear evidence and readback are retained. An empty stored-memory readback does not erase or hide current faults.
- No live-data dashboard, adaptation-reset, coding or actuator-test UI is supplied in Lite.
- The shared collector names files `HFMreader_V2_*.zip` and includes unused acquisition-coverage fields. These are not claims that Lite acquired live data or completed V2 validation.
- The Windows executable is unsigned. Adapter drivers are separate. Launch from a writable local extracted folder; preserve `_internal`.
- New users create their own local logs. Logs may contain ECU identification, user-entered labels and exception details; review before sharing. No automatic upload occurs.
