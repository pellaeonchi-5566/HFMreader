# Submit Vehicle Test Results & Logs

We invite Mercedes-Benz HFM owners worldwide to contribute voluntary real-vehicle results, not just bug reports. Successful sessions are valuable evidence too. Successful, Partially Successful, Failed and Connection Failed results are all welcome. Do not perform extra DTC clears or learning-value resets just to improve a report.

## Create and review your test ZIP

1. Stop reading, disconnect and close HFMreader.
2. In the extracted application folder, run **PACKAGE_RESULTS.cmd**. It packages results locally; it does not upload anything.
3. Read **PACKAGE_RESULTS.txt** for the result and ZIP location. Open the generated **HFMreader_RESULTS_*.zip** and inspect its contents. If packaging fails, retain your original logs and describe the failure in your report.
4. Check for names, VIN/registration information, private paths or annotations, unrelated captures and other people's data. Keep an untouched copy privately; remove information you do not want to share from the submission copy and describe any redaction. Do not submit another person's data without permission.

The bundle may contain logs, captures, control logs, PC_CHECK.txt and a build manifest. Complete session logs help analysis more than isolated screenshots, including when connection fails.

## Submit through GitHub

1. Open [New Issue](https://github.com/pellaeonchi-5566/HFMreader/issues/new/choose) and select **Submit Vehicle Test Results & Logs**. Sign in to GitHub if needed.
2. Fill in the model, year, engine, ECU part number, interface, Windows version and HFMreader version once. Use Unknown for information you cannot obtain; do not guess or provide a private VIN.
3. Select **Successful**, **Partially Successful**, **Failed** or **Connection Failed**. State whether this was a real vehicle or simulation, the ignition/engine conditions and the operations attempted. Distinguish no request sent, communication failure, no valid data and a valid response. A read attempt alone is not full vehicle validation.
4. Optionally use **Reviewed test ZIP** to select or drag in HFMreader_RESULTS_*.zip. Full reviewed logs are encouraged, but attachments are not required. GitHub currently documents a 25 MB ZIP limit; if rejected, submit the result without the file and agree on another transfer method with the maintainer. No private inbox is currently promised.
5. Review the privacy and analysis statement, then submit the Issue. Do not repeat vehicle or computer details in the narrative unless needed to explain a difference.

## Privacy and permitted analysis

Logs are submitted voluntarily and are never uploaded automatically. By submitting data, you allow the HFMreader team to analyze it for ECU compatibility, diagnostic protocols and communication problems. Public Issue attachments can be accessed by other people. You may omit attachments; agree on a private transfer method with the maintainer before sending private files. Further public sharing of your original personal logs by the team will remain within your consent; submission is not blanket permission to republish them elsewhere.

Do not attach private files to a public Issue expecting confidentiality. You can report a result without publicly attaching any logs. Do not post credentials or private download tokens. Keep your original logs after reporting.

Upload field reference: [GitHub form schema](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests/syntax-for-githubs-form-schema#upload).
