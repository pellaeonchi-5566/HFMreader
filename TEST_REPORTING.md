# Submit Vehicle Test Results & Logs

Success is useful research evidence, not just failure. Select **Successful**, **Partially Successful**, **Failed**, or **Connection Failed**.

## Lite V1 Public Test 1

1. Attempt F1 identification and F3 fault reading. No clear operation is required for a report.
2. Press **F7**; F2/disconnect and Esc/close also package evidence. Open `logs/lite` beside the application. Keep this entire folder locally, including failed attempts and pre-clear archives.
3. Open the resulting **HFMreader_V2_*.zip** and confirm `sessions/.../events.jsonl` and `summary.json` exist. The inherited V2 filename does not identify the software edition; report **Lite V1 Public Test 1**. Simulation lives in `logs/lite_simulation` and must be reported as simulation.
4. Review the archive for names, labels, identification and other information you do not want public. Describe any redaction. If packaging failed, preserve raw logs and report the error.
5. Open [the vehicle test form](https://github.com/pellaeonchi-5566/HFMreader/issues/new?template=vehicle-test.yml). Enter vehicle model/year/engine, ECU identification, interface/driver, Windows and software version. Unknown is acceptable. Select the outcome and describe ignition/engine conditions and steps attempted; avoid repeating the identification fields.
6. Optionally attach the reviewed ZIP. Include an independent diagnostic result if available, specifying whether the same vehicle, interface and wiring were used. Complete logs are encouraged; screenshots alone often omit the failed transaction.

For **older full HFMreader builds**, the existing `PACKAGE_RESULTS.cmd` produces `HFMreader_RESULTS_*.zip`. Lite instead uses F7; it does not include that older command.

Submitting is voluntary. No files are uploaded automatically. Public Issue attachments can be accessed by others; you may omit attachments or agree on a private transfer method with the maintainer before sending private files. Submission allows HFMreader team analysis of ECU compatibility, diagnostic protocols and communication problems. Further team sharing of original personal logs must remain within your consent; it is not blanket permission for republication elsewhere.
