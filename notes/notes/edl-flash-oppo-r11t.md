# OPPO R11T EDL(9008) Flash Experiment
## Experiment Overview
Test Qualcomm EDL 9008 download mode, extract firmware, boot.img extraction and partition repair.

## Environment
- Device: OPPO R11T
- Tool: MsmDownloadTool
- Firmware: OFP full firmware package

## Key Operation
1. Enter EDL 9008 mode by key combination.
2. Load ofp firmware in MsmDownloadTool.
3. Extract boot.img from firmware.
4. Problem encountered: NV partition damaged, IMEI becomes 0.
5. Attempt to flash TWRP recovery via EDL.

## Conclusion
- 9008 can write raw partitions at low level.
- Damaged NV partition leads to baseband abnormal.
- Unlock BL of old OPPO devices has strict version limit.

## Statement
Only personal learning experiment, not for commercial or illegal use.
