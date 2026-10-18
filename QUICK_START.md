# Quick start

1. Use a Windows 10/11 x64 computer. Extract the entire ZIP to a writable local folder, such as Documents/HFMreader. Do not run inside the ZIP or move the EXE away from _internal.
2. Before visiting the vehicle, run CHECK_PC.cmd and inspect PC_CHECK.txt: "passed": true. Run SIMULATE.cmd, F1 to connect, F9/F10 to change data pages, F2 to disconnect, then Esc to exit. Simulation cannot prove cable or vehicle compatibility.
Read HARDWARE_CONNECTION.md for the two cables and the exact distinction between OBD-side and vehicle-side pin numbers.

3. Install the driver supplied for your compatible USB K-Line interface. Confirm its COM number in Windows Device Manager. Match the interface and vehicle diagnostic connector wiring to the vehicle's documented HFM pinout; a mechanically fitting adapter does not establish electrical compatibility. Do not guess pin assignments.
4. With the vehicle safely stationary, parking brake applied and transmission in P/N, connect the verified interface. Keep cables away from pedals and moving/hot parts. Use the ignition state required by the operation; do not perform control operations while driving. Stable vehicle supply is required.
5. Run START.cmd. Tab to the COM selector and use arrow keys to choose the verified port. F1 connects; F4 shows identification. Check ECU identity before interpreting results. F2 disconnects. F3 pauses/resumes live reading.
6. F9/F10 change live-data pages; left/right change status pages outside text/selection fields. F8 opens settings: Tab/arrow keys, Enter to apply, Esc to cancel. Disconnect before changing polling settings. Ctrl+D opens selected data details. Ctrl+E switches English/Chinese.
7. F5 reads DTCs. Save pre-clear evidence first. F6 opens the existing clear confirmation; cancellation must remain available. Ctrl+Shift+R prepares learning-value reset, with the existing confirmation and ECU conditions. Ctrl+Shift+I requests post-reset readback. Reset can change adaptation; do not assume it is equivalent to a read-only operation.
8. F12 controls the existing conditional read experiment, only while disconnected and only within its explicit ECU restriction. Its confirmation does not establish compatibility with other ECUs.
9. F7 exports logs. Disconnect with F2 and allow completion, then Esc to close. Run PACKAGE_RESULTS.cmd after closing. Read PACKAGE_RESULTS.txt for the result ZIP location or an error.
10. Before leaving, confirm logs exists, contains this session's files, and the result ZIP opens. Keep the entire logs and control_logs folders even if packaging fails. Follow TEST_REPORTING.md before sharing.

If communication fails, stop the operation and keep its logs. Do not repeatedly press clear/reset or treat a timeout as proof that a command was never received. Reconnect only after checking ignition, supply, cable and COM settings. No new live control experiment is required for initial participation.
