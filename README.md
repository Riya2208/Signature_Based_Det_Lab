# Signature-based detection lab

## Overview

This lab demonstrates basic signature-based detection steps: download sample archive, inspect files, extract safely, and record file checksums (SHA256 and MD5) for signature creation and tracking.

**Safety:** Do **not** execute any unknown binaries (e.g., `test.exe`) on your host. Work inside an isolated VM or sandbox (air-gapped VM, snapshot before testing). Treat all files as malicious until proven otherwise.

---

## Files / folders

* `signature_lab/` — project root
* `malz.zip` — sample archive (password: `infected`)
* `extracted/` — files extracted from `malz.zip`
* `checksums/` — saved checksum files

---

## Notes

* Keep all operations inside an isolated environment.
* Do not commit real malware samples to a public repository — only commit logs, checksums, and sanitized outputs.
