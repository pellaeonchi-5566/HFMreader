# Known issues and limitations

- Experimental public test, not a universal diagnostic tool or a certified repair decision system.
- Most extensive field evidence: BOSCH 0135451332 / 41/00. Other variants require their own evidence. Existing ECU gates remain active.
- Intermittent echo/synchronization, timeouts and disconnects remain possible. Raw transactions, timestamps and explicit missing/error states matter more than an isolated display value.
- The 29 HHT runtime records include conditional and incompletely interpreted signals. A response is not proof of physical meaning or universal applicability.
- 31 DTC descriptions are unverified and show the number with a placeholder. Codes 107/117 have supported core meanings but uncertain detailed conditions. Equipment-reference descriptions retain scope notes. Labels 0/1 are application labels, not asserted digital HHT fault definitions.
- DTC clearing removes diagnostic evidence; learning-value reset changes ECU adaptation state. Read/save first and observe the existing confirmations. Never assume a failed response proves no state change.
- The Windows EXE is unsigned. SmartScreen or antivirus behavior has not been certified across machines.
- No new vehicle test is implied by offline test results. Windows versions, adapters and ECU combinations not explicitly tested remain unverified.
- Logs and exported ZIPs may contain ECU identity, timestamps, COM information, user-entered annotations and local session paths. Review before sharing.
- Compiled Python packaging avoids directly readable application source files; it is not a guarantee against reverse engineering.
