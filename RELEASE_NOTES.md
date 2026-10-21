# HFMreader 1.1.1-public.1 — connection recovery maintenance

This experimental update improves host-side cleanup after a failed read.
It does not establish the cause of intermittent field failures and does not
guarantee that USB unplug/replug will no longer be necessary.

- A responsive COM worker gets a bounded normal-close attempt after failure.
- A stalled worker remains subject to forced termination.
- Original communication errors and cleanup errors are preserved separately.
- Logs include child PID/exit status, cleanup duration and partial RX.
- Windows CloseHandle failure is reported instead of silently ignored.
- No automatic command replay/reconnect; reconnect explicitly.

Existing pages, keyboard controls, formulas, read recipes, timing, DTC clearing,
adaptation reset and their safeguards remain unchanged. No new actuator feature.
Offline regression and clean-package checks are not a new vehicle validation.

Extract this ZIP into a new folder. Keep older logs/packages for comparison.
Run CHECK_PC.cmd, then SIMULATE.cmd before connecting your stationary vehicle.
On failure, try normal disconnect/reconnect; if it fails, close and reopen the
application without unplugging USB, then try USB reconnect only if needed.
Record which step restored operation. Do not operate the computer while driving.
Before leaving, use PACKAGE_RESULTS.cmd and verify the resulting ZIP exists.
Review logs for personal data before voluntarily sharing them.

繁體中文：本版改善讀取失敗後的 COM 清理與紀錄，尚未實車證明能消除斷線。
請解壓至新資料夾，先執行 CHECK_PC.cmd 與 SIMULATE.cmd。停車時測試重新連線、
關閉重開程式，再視需要拔插 USB，記下哪一步恢復。離開前執行 PACKAGE_RESULTS.cmd，
確認產生 HFMreader_RESULTS_*.zip。保留舊版與原始紀錄。
