# Lite quick start

1. Download the complete **HFMreader_Lite_V1_public.1_WIN64.zip** release asset and extract it to a writable local folder. Keep `_internal` beside the EXE. No Python installation is needed.
2. Run `CHECK_PC.cmd`. Read `CHECK_PC_RESULT.json`: `passed` must be `true`. This offline check creates a simulation session and tests GUI, background process, reading and export. It does not open a physical COM port.
3. Run `SIMULATE.cmd`. F1 connects to simulated data, F3 reads simulated fault memory, F6 changes language and F7 exports. The title explicitly says SIMULATION. Close it before vehicle testing.
4. Install the correct adapter manufacturer's Windows driver, confirm its COM number in Device Manager, and verify wiring using [HARDWARE_CONNECTION.md](HARDWARE_CONNECTION.md). Drivers are not bundled. Close other diagnostic programs that may own the same port.
5. With the vehicle parked, ignition ON and engine OFF, run `Start_Lite.cmd`. Tab to COM, enter/select the port, then F1 to connect/read identification. F3 reads faults. No ECU selection profile is required.
6. Record the result, including failures. Compare with an independent diagnostic tool if available; close HFMreader's connection before another tool uses the adapter. F2 disconnects; F1/F3 repeats the attempt.
7. F4 is optional and state-changing. Use it only when clearing is intended, after saving evidence. Read and explicitly confirm the warning. A failed clear is not automatically retried; reconnect and inspect memory before any further decision.
8. F7 exports; F2 and Esc also package logs. Before leaving the vehicle, verify `logs/lite` contains a ZIP with `sessions/.../events.jsonl` and `summary.json`. Keep the entire `logs/lite` folder. If export fails, keep the raw folder; do not overwrite it.

Use Tab, arrow keys, Enter and Escape for dialogs. No road-driving test is requested. Optional parked idling can document current faults, but do not clear while the engine is running. See [中文操作卡](LITE_START_ZH_TW.md).
